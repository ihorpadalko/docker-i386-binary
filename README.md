# docker-i386-binary

This is a full set of Docker 17.05.0-ce binaries build from a source code to be run on 32bit system. 
The package contains:

`dockerd` - The Docker daemon itself. The highest level component in your list and also the only 'Docker' product listed. Provides all the nice UX features of Docker.
version: 17.05.0-ce
build: 89658be

`(docker-)containerd` - Also a daemon, listening on a Unix socket, exposes gRPC endpoints. Handles all the low-level container management tasks, storage, image distribution, network attachment, etc...
version: 0.2.3 
commit: 9048e5e50717ea4497b757314bad98ea3763c145

`(docker-)containerd-ctr` - A lightweight CLI to directly communicate with containerd. Think of it as how 'docker' is to 'dockerd'.
version: 0.2.3 
commit: 9048e5e50717ea4497b757314bad98ea3763c145

`(docker-)containerd-shim` - After runC actually runs the container, it exits (allowing us to not have any long-running processes responsible for our containers). The shim is the component which sits between containerd and runc to facilitate this.

`(docker-)runc` - A lightweight binary for actually running containers. Deals with the low-level interfacing with Linux capabilities like cgroups, namespaces, etc...
version:    1.0.0-rc2
commit: c91b5bea4830a57eac7882d7455d59518cdf70ec