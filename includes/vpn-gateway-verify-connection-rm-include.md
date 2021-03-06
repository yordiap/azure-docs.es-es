### <a name="to-verify-your-connection-by-using-powershell"></a>Para comprobar la conexión mediante PowerShell

Puede comprobar que la conexión se realizó correctamente mediante el uso del cmdlet "Get-AzureRmVirtualNetworkGatewayConnection", con o sin "-Debug". 

1. Puede usar el siguiente ejemplo de cmdlet, configurando los valores para que coincidan con los tuyos. Cuando se le pida, seleccione "A" para ejecutar "todo". En el ejemplo, "-Name" hace referencia al nombre de la conexión que creó y quiere probar.

  ```powershell
  Get-AzureRmVirtualNetworkGatewayConnection -Name MyGWConnection -ResourceGroupName MyRG
  ```
2. Cuando el cmdlet haya finalizado, consulte los valores. En el ejemplo siguiente, el estado de conexión aparece como "Conectado" y pueden verse los bytes de entrada y salida.

  ```
  "connectionType": "IPsec",
  "routingWeight": 10,
  "sharedKey": "abc123",
  "connectionStatus": "Connected",
  "ingressBytesTransferred": 33509044,
  "egressBytesTransferred": 4142431
  ```

### <a name="to-verify-your-connection-by-using-the-azure-portal"></a>Para comprobar la conexión mediante el Portal de Azure

En el Portal de Azure, puede ver el estado de conexión navegando a la conexión. Hay varias formas de hacerlo. Los pasos siguientes muestran una manera de navegar a su conexión y realizar las comprobaciones necesarias.

1. En [Azure Portal](http://portal.azure.com), haga clic en **Todos los recursos** y navegue a la puerta de enlace de la red virtual.
2. En la hoja de la puerta de enlace de la red virtual, haga clic en **Conexiones**. Puede ver el estado de cada conexión.
3. Haga clic en el nombre de la conexión que desee comprobar para abrir **Essentials**. En Essentials, puede ver más información acerca de la conexión. El valor de **Estado** será "Correcto" y "Conectado" cuando haya realizado una conexión satisfactoria.
   
    ![Comprobación de la conexión](./media/vpn-gateway-verify-connection-rm-include/connectionsucceeded.png)