# Batch Connect - OSC Owens Desktop

![GitHub Release](https://img.shields.io/github/release/osc/bc_osc_owens_desktop.svg)
![GitHub License](https://img.shields.io/github/license/osc/bc_osc_owens_desktop.svg)

A VNCSim app designed for OSC OnDemand that launches a Desktop within an Owens
batch job.

## Install

Use git to clone this app and checkout the desired branch/version you want to
use:

```sh
git clone <repo>
cd <dir>
git checkout <tag/branch>
```

You will not need to do anything beyond this as all necessary assets are
installed. You will also not need to restart this app as it isn't a Passenger
app.

To update the app you would:

```sh
cd <dir>
git fetch
git checkout <tag/branch>
```

Again, you do not need to restart the app as it isn't a Passenger app.

For **development** you will need to use
[bower](https://www.npmjs.com/package/bower) to update the assets for this app:

```sh
bower install
bower prune
```

followed by versioning them if they have changed.

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
