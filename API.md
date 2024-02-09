<a name="USB2SNES"></a>

## USB2SNES
Client for the USB2SNES WebSocket server

**Kind**: global class  

* [USB2SNES](#USB2SNES)
    * [new USB2SNES(addr)](#new_USB2SNES_new)
    * _instance_
        * [.init()](#USB2SNES+init) ⇒ <code>Promise</code>
        * [.sendImmediate(opcode, [opt_operands], [opt_flags], [opt_space])](#USB2SNES+sendImmediate)
        * [.send(opcode, [opt_operands], [opt_flags], [opt_space])](#USB2SNES+send) ⇒ <code>Promise.&lt;(object\|buffer)&gt;</code>
        * [.addErrorListener(handler)](#USB2SNES+addErrorListener)
        * [.addCloseListener(handler)](#USB2SNES+addCloseListener)
        * [.close()](#USB2SNES+close)
    * _static_
        * [.Keys](#USB2SNES.Keys)
        * [.Spaces](#USB2SNES.Spaces)
        * [.Opcodes](#USB2SNES.Opcodes)

<a name="new_USB2SNES_new"></a>

### new USB2SNES(addr)

| Param | Type |
| --- | --- |
| addr | <code>string</code> | 

<a name="USB2SNES+init"></a>

### usB2SNES.init() ⇒ <code>Promise</code>
Initialize the WebSocket client

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  
<a name="USB2SNES+sendImmediate"></a>

### usB2SNES.sendImmediate(opcode, [opt_operands], [opt_flags], [opt_space])
Immediately send a command to the WebSocket server. Does not resolve any result.
Use only for opcodes that do not trigger a response from the server, such as "Attach" and "Name".
Otherwise, use this.send.

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  

| Param | Type |
| --- | --- |
| opcode | <code>string</code> | 
| [opt_operands] | <code>Array</code> | 
| [opt_flags] | <code>Array</code> | 
| [opt_space] | <code>string</code> | 

<a name="USB2SNES+send"></a>

### usB2SNES.send(opcode, [opt_operands], [opt_flags], [opt_space]) ⇒ <code>Promise.&lt;(object\|buffer)&gt;</code>
Send a command to the WebSocket server. Returns a promise that eventually resolves the result based on the command queue.

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  

| Param | Type |
| --- | --- |
| opcode | <code>string</code> | 
| [opt_operands] | <code>Array</code> | 
| [opt_flags] | <code>Array</code> | 
| [opt_space] | <code>string</code> | 

<a name="USB2SNES+addErrorListener"></a>

### usB2SNES.addErrorListener(handler)
Add an error handler to the WebSocket client

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  

| Param | Type |
| --- | --- |
| handler | <code>function</code> | 

<a name="USB2SNES+addCloseListener"></a>

### usB2SNES.addCloseListener(handler)
Add an close handler to the WebSocket client

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  

| Param | Type |
| --- | --- |
| handler | <code>function</code> | 

<a name="USB2SNES+close"></a>

### usB2SNES.close()
Close the WebSocket client

**Kind**: instance method of [<code>USB2SNES</code>](#USB2SNES)  
**Access**: public  
<a name="USB2SNES.Keys"></a>

### USB2SNES.Keys
Keys for a USB2SNES command object/response: https://github.com/Skarsnik/QUsb2snes/blob/master/docs/Protocol.md#performing-a-request

**Kind**: static property of [<code>USB2SNES</code>](#USB2SNES)  
<a name="USB2SNES.Spaces"></a>

### USB2SNES.Spaces
Valid spaces for a command: https://github.com/Skarsnik/QUsb2snes/blob/master/docs/Protocol.md#performing-a-request

**Kind**: static property of [<code>USB2SNES</code>](#USB2SNES)  
<a name="USB2SNES.Opcodes"></a>

### USB2SNES.Opcodes
USB2SNES opcodes from https://github.com/Skarsnik/QUsb2snes/blob/687455a4c32d8e0712611950d9ad368facc4d40a/usb2snes.h#L104

**Kind**: static property of [<code>USB2SNES</code>](#USB2SNES)  
