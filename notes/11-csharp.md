# CSharp

Postman Test 10/4

Socket is a messaging system between server and client
WS button in network tab

Socket_authenticated(received messages)
  red
  green: messages we send

  Socket Service and Handler(similar to controlller) tell us what to do when we receive a message, but dont respond

  only one type of send() == message 

  no async

  socketSErvivice.emit('SOCKET_TEST')

socketProvicder.message('USER_LOGGED_IN') == on the server

You can see any action on the server side from anywhere

Use a auth socket to queue up requests while you are waiting for authorization. Only sends when you are logged in.