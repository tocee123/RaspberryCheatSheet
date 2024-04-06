1. open `powershell` in admin mode
2. `wsl --shutdown`
3. `Get-Service vmcompute | Restart-Service`
4. `wsl`

If it won't work, because `docker-desktop` and `docker-desktop-data` is not starting up, you can reinstall the underlying distro to ubuntu. Use the following:
1. `wsl -l -v --all` / list all distros
2. `wslconfig /unregister docker-desktop`
3. `wslconfig /unregister docker-desktop-data`
4. `wsl --install --distribution ubuntu`
