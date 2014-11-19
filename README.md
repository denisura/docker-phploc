docker-phploc
=============

Run phploc in Docker container. A tool for quickly measuring the size of a PHP project. 


Build
--------------------

Build from `Dockerfile`:

    ``` sh
    sudo docker build -t denisura/phploc .
    ```

Verify build:

    ``` sh
    sudo docker run --rm -it denisura/phploc --version
    ```

Usage
--------------------

1. Install the `denisura/phploc` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/phploc
    ```

2. Define an bash alias that runs this container whenever `phploc` is invoked on the command line:

	``` sh
	$ echo "alias phploc='docker run --rm -it -v \$(pwd):/workspace denisura/phploc'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run phploc as always:

	``` sh
	$ phploc --version
	```
