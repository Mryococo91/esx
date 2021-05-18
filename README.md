# ESX

ESX v1, Hawaii Edition. My continued efforts to improve ESX. After snake gizz kicked me off ESX he and the new members ruined the, now called _legacy_ branch I'll let y'all keep speculating why he isn't ever going online again.

The point of this repo is not to replace the mainstream ESX installation, ever. It's intended to teach people of improvements that could be made to the framework. I'll keep making breaking changes to improve the framework. Improvements made are mainly optimizations so you can run >100 players with it, which you definitely cannot run with the original code.

It also doesn't come with a inventory since you shouldn't be using that garbage UI for that, make/ use a better one. Probably more things "missing" from the original ESX experience.

[For those who want to be a part of the continued **development**, there's a discord](https://discord.gg/H86eaEPwvK) (H86eaEPwvK)

## Improvements over ESX

- Server performance improvements, such as saving player data
- Supports multiple character scripts such as kashacters
- Supports multiple groups
- Vehicles don't despawn ever

## Installation

### Configuration File

You need to setup the proper permissions for ESX for it to handle your server

```
add_ace resource.esx command.add_ace allow
add_ace resource.esx command.add_principal allow
add_ace resource.esx command.remove_principal allow

# Setup Group Inhereances
add_principal group.user builtin.everyone

add_principal group.donator_level_1 group.user
add_principal group.donator_level_2 group.donator_level_1
add_principal group.donator_level_3 group.donator_level_2

add_principal group.dev_level_1 group.user
add_principal group.dev_level_2 group.dev_level_1

add_principal group.staff_level_1 group.user
add_principal group.staff_level_2 group.staff_level_1
add_principal group.staff_level_3 group.staff_level_2
add_principal group.staff_level_4 group.staff_level_3
add_principal group.staff_level_5 group.staff_level_4
add_principal system.console group.staff_level_5
```
