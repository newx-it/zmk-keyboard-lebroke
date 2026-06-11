add the lebroke zmk config repository by modifying your west.yml file in config. then, add a copy of the `.conf` file and the `.keymap` file.

```manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    # Add the base GitHub URL as a remote.
    - name: newx-it
      url-base: https://github.com/newx-it
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    # Add the name of the repository as a project.
    - name: lebroke-zmk-config
      remote: newx-it
      revision: main
  self:
    path: config```