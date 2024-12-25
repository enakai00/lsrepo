lsrepo
======

Search private Docker registry


## Usage

```
 # lsrepo REGISTRY [REPOSITORY]
```


## Example

```
# lsrrepo myregistry.example.com:5000
REPOSITORY                        TAG                 IMAGE ID    
enakai00/centos                   centos6             b1bd49907d55
enakai00/centos                   centos7             b157b77b1a65
enakai00/centos                   latest              b157b77b1a65
enakai00/fedora                   20                  88b42ffd1f7c
supertest2014/nyan                latest              a61f7f4d8006 
```


```
# lsrrepo myregistry.example.com:5000 enakai00/centos
REPOSITORY                        TAG                 IMAGE ID    
enakai00/centos                   centos6             b1bd49907d55
enakai00/centos                   centos7             b157b77b1a65
enakai00/centos                   latest              b157b77b1a65
```


## How to run your private registry

You can use an official registry image from https://registry.hub.docker.com/_/registry/

```
# mkdir /var/lib/docker-registry
# docker run -itd -p 5000:5000 -v /var/lib/docker-registry:/tmp/registry --name myregistry registry
```

