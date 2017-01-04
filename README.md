# Batch Connect - OSC Owens Desktop

![GitHub Release](https://img.shields.io/github/release/osc/bc_osc_owens_desktop.svg)
![GitHub License](https://img.shields.io/github/license/osc/bc_osc_owens_desktop.svg)

A VNCSim app designed for OSC OnDemand that launches a Desktop within an Owens
batch job.

## Install

1. Git clone this app in the desired location and go into the directory:

  ```sh
  git clone <repo> bc_osc_owens_desktop

  cd bc_osc_owens_desktop
  ```

2. Checkout the version of the app you want to deploy:

  ```sh
  git checkout <tag>
  ```

2. This app requires the [bc_desktop](https://github.com/OSC/bc_desktop) Bower
   asset, so we will need a local copy of Bower:

   ```sh
   npm install bower
   ```

3. Install the Bower asset:

  ```sh
  node_modules/.bin/bower install
  ```

## Update

1. Fetch the updated code:

  ```sh
  git fetch
  ```

2. Checkout the desired tag:

  ```sh
  git checkout <tag>
  ```

3. Update the Bower assets:

  ```sh
  node_modules/.bin/bower update --force
  ```

## Specification

### ROOT

All assets in this package look for dependencies in the specified `$ROOT`
directory. This should be set to correspond to the included `template/`
directory.

An example running the `xstartup` script included in this package:

```sh
# Path where you installed this project
BC_OSC_OWENS_DESKTOP_DIR="/path/to/bc_osc_owens_desktop/template"

# Run the `xstartup` script with proper `$ROOT` set
ROOT="${BC_OSC_OWENS_DESKTOP_DIR}" ${BC_OSC_OWENS_DESKTOP_DIR}/xstartup
```

## Contributing

1. Fork it ( https://github.com/OSC/bc_osc_owens_desktop/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
