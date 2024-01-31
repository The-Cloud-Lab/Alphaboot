# Alphaboot:Accelerated Container Cold Start

Alphaboot helps to cache container images locally to reduce the cold boot time.

To install Alphaboot follow the following steps:

1) ```git clone https://github.com/The-Cloud-Lab/Alphaboot.git    ```

2) ```cd Alphaboot``` (change directory into the fork)

3) From the root of the forked alphaboot directory run ```sudo make```

4) This creates the dockerd binary in bundles/binary-daemon/dockerd.

5) Stop the docker service if it is already running using ```sudo service docker stop```

6) Replace the binary of the installed Docker service with the one we just created by running ```sudo cp bundles/binary-daemon/dockerd /usr/bin/```

7) Start the docker service ```sudo service docker start ```

Alphaboot caches container images locally everytime a new image is fetched from an online registry.
After an image is cached next time when the same image is required the image is fetched directly from the cache instead of the online registry saving the cold boot time.
