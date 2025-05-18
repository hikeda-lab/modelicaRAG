


## macOSでのdockerの OpenModelicaの動かし方

Docker側のdisplayのIPアドレスを特定する。


```shell
❯ docker-om OMEdit
Authorization required, but no authorization protocol specified
qt.qpa.xcb: could not connect to display 192.168.1.22:0
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found.
This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem.

Available platform plugins are: eglfs, linuxfb, minimal, minimalegl, offscreen, vnc, xcb.
```


```shell
❯ xhost
access control enabled, only authorized clients can connect
LOCAL:
```


```shell
❯ xhost +192.168.1.22
192.168.1.22 being added to access control list
❯ docker-om OMEdit
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-'
libGL error: No matching fbConfigs or visuals found
libGL error: failed to load driver: swrast

```