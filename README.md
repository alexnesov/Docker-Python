<H4> Launching a Python Flask runtime container</H4>

Go in the required folder (in my case here, the one containing ```flask_example.py```):

```docker run -it --name myflask1 -p 5000:5000```

<ul>
<li><code>docker run</code> simply start a new container </br>
<li><code>-it</code> allows for an interactive container with output in terminal window </br>
<li><code>-p 5000:5000</code> defines the port mapping. Every container has it own network stack, own IP address, etc... Flask waits for http requests at this defined port (5000). 5000 on the left is Host Port, 5000 on the right side of the column is the container port. Thanks to this mapping we can access the container with <code>localhost:5000</code> urli
<li><code>-v ${PWD}:/app </code>This option mapps current working directory on development machine denoted by <code>PWD</code> variable to <code>/app</code> directory in the container. This way, the container is going to have access to all filles and sub-folders of basic env folder. Programs run in the container can read and write to <code>/app</code> directory. This way they acces basic env.This is called <strong>bind mounting</strong>.
</ul>
