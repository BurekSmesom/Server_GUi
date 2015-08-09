# Server_GUi
Java multithreading server


Structure project:
1.inputServer
2.MultiThreadServer
3.Server
4.ServerFrame
5.ServerGui

Main java-class is "ServerGui" - class , there all start. "ServerGui" - class calls "server_main" - function, there is loop for waiting connections from clients, when (socket.accept)  clients connect,  it creates new Thread - "MultiThreadServer" - class, "MultiThreadServer" - class on one side creates new thread, waiting for incomming messages "inputServer" - class, and on other side frame "ServerFrame". "ServerFrame" contains textField for input from server side (message) to send, and textArea, for displaying messages from client and from you. There is also "Server" - class for in command promt run program.
Issue is when i wanna to close ServerSocket in class "ServerGui" - class, others, client sockets that in meanwhile was made, they still running. Try with simple telnet to stop server on button.
