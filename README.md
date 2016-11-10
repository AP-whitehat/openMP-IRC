<h4>An IRC made as an personal Project/Assignment</h4>

I don't intend to infringe copyrights 

<h3>#CREDITS</h3>
Code starting template
<a href="http://berenger.eu/blog/c-a-tcpip-server-using-openmp-linux-socket/" > A tcp/ip server using OpenMP </a> <br>
Pacheco Introduction To Parallel Programming Morgan Kaufmann (openMP concepts) <br>
www.tutorialspoint.com/unix_sockets/index.htm (for understanding Sockets & networking ) <br>
www.linuxhowtos.org/C_C++/socket.htm (for understanding Sockets & networking) <br>
<a href="berenger.eu/blog/">Berenger Bramas's blog </a>    (for multithreading & HPC) <br>
<a href="http://beej.us/guide/bgnet/output/html/singlepage/bgnet.html" > Beej's guide to networks </a> (for network/socket system calls reference )
<br>
<h2> Introduction </h2>
This uses NON-Blocking sockets to communicate between server and client 
Uses openMP to handle multiple clients .
<br><h4>Salient features</h4>
<br>
<ul>
<li> Multiple clients can chat with each other simultaneously </li>
<li>Msg by Nickname and by channel </li>
<li>Message waits for offline client </li>
<br>
<p><h2>How to use</h2><br></p>
<h3> Client</h3>

To Setup a client , one need to compile the client.cpp onto their pc . <br>
call the client with hostname of the server and respective port <br>
<code> ./client hostname portno </code> <br>

<h4> Manual </h4>
For single one to one msg <br>
<code> /msg nick "your message" </code> <br>
For channel msg <br>
<code> /cmsg chname "your meassage" </code><br>
For public broadcast <br>
<code> /all "your message" </code><br>
To create a new channel <br>
<code> /add channelname </code> <br>
To join a channel <br>
<code> /join channelname </code> <br>
To quit your client <br>
<code> quit </code> <br>

<h3> Server </h3>

To setup Server , one needs to compile server.cpp with server.h . <br>
Simple right ? , NO it gets a little tricky 
your gcc version must support openMP and copilation needs to done with an 
<code> -fopenmp </code> option

Refer <a href="https://www.dartmouth.edu/~rc/classes/intro_openmp/compile_run.html" > how to compile openMP Programs</a>

