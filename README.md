# GPG-ioctl-FiX

Error is like
```
gpg: problem with the agent: ...ioctl...
```

FiX:
```
nano ~/.gnupg/gpg.conf
add this --> use-agent 
add this --> pinentry-mode loopback
```

```
nano  ~/.gnupg/gpg-agent.conf
add this --> allow-loopback-pinentry
```

```
restart the agent
echo RELOADAGENT | gpg-connect-agent
```
