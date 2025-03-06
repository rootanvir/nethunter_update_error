# nethunter_update_error
## Error Message
```
┌──(root㉿kali)-[/]
└─#  sudo apt update
Ign:1 http://http.kali.org/kali kali-rolling InRelease
Ign:1 http://http.kali.org/kali kali-rolling InRelease
Ign:1 http://http.kali.org/kali kali-rolling InRelease
Err:1 http://http.kali.org/kali kali-rolling InRelease
  Temporary failure resolving 'http.kali.org'
1321 packages can be upgraded. Run 'apt list --upgradable' to see them.
Warning: Failed to fetch http://http.kali.org/kali/dists/kali-rolling/InRelease  Temporary failure resolving 'http.kali.org'
Warning: Some index files failed to download. They have been ignored, or old ones used instead.
```
## Solve : run those command
```
echo 'APT::Sandbox::User "root";' > /etc/apt/apt.conf.d/01-android-nosandbox
```
```
groupadd -g 3003 aid_inet && usermod -G nogroup -g aid_inet _apt
```
