# Welcome to Mojo 🔥

Mojo is a new programming language that bridges the gap between research 
and production by combining Python syntax and ecosystem with systems 
programming and metaprogramming features. Mojo is still young, but it is designed
to become a superset of Python over time. 

[github.com/modularml/mojo](https://github.com/modularml/mojo)


## Getting Started
### Mojo SDK Container

The repo also contains a Dockerfile that can be used to create a  
Mojo SDK container for developing and running Mojo programs. Use the  
container in conjunction with the Visual Studio Code devcontainers  
extension to develop directly inside the container.

The Dockerfile also sets up a `conda` environment and by default,  
starts a `jupyter` server (which you can access via the browser).

To build a Mojo container, use the convenience script provided:

```bash
./build-image.sh --auth-key <your-modular-auth-key> --mojo-version 0.3
```

In the example below,  
we map the ports, bind mount the current directory:

```bash
docker run \
   -it \
   --network=host \
   --name=mojo \
   -v ${PWD}:/workspace \
   holmen1/mojosdk:latest
```

In VSCode, you can now use the `Attach to Running Container` command to
attach to the container and start developing.

```bash
mojo /workspace/hello.🔥
```

```python
Hello Mojo 🔥!
9
6
3
```

Create a stand-alone executable with the build command:
```bash
mojo build hello.🔥
```

Then run the executable:
```bash
./hello
```

