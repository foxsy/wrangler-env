# wrangler-env
Easy way to switch between Cloudflare wrangler profiles

Include `wrangler-env` in your bash profile config (~/.profile,  ~/.bash_profile, or ~/.bashrc) by adding:

```
 # Wrangler Profile Switcher
  export CF_WRANGLER_PROFILES=~/.wrangler/profiles
  . ~/bin/wrangler-env
```

After that you can use it with: `wrangler-switch <profile name>`
*Note: If you have fzf installed you don't have to supply a profile name and it will get you a list of profiles to select*

By default it will load the profile set in CF_WRANGLER_PROFILES/default at the shell initialization. 

Other commands are: 
 * `wrangler-unset` will unset the env variables being set to the default
 * `wrangler-list` will list all of the profiles in your profile directory (CF_WRANGLER_PROFILES)
 * `wrangler-who` shows the current profile being set