# Rojo CI/CD Test
This project tests automatic deployment of Roblox places from GitHub. It's aiming to demonstrate a complete CI/CD (continuous integration/continuous deployment) pipeline that's common elsewhere in the software industry.

This project be updated as features and improvements are made to Rojo.

Tools:
* Rojo `master`
* Lemur
* Travis-CI

## Usage
You'll need the latest `master` of Rojo installed. You can do that by cloning the Rojo repository somewhere and using `cargo install` an extra argument:

```sh
git clone https://github.com/LPGhatguy/rojo.git
cargo install --path rojo
```

If you already have Rojo installed, you can use `--force` to overwrite it.

**Note that the current Rojo `master` branch is incompatible with 0.4.x, so you may need to revert when you're done experimenting with this repository.**

### Generating the Place File
```sh
rojo build --output Test.rbxl
```

### Deploying the Place
```sh
rojo upload --cookie [security cookie] --place_id [place id]
```

### Developing in the place file
Install the current Rojo `master` plugin. Docs for how to do this easily are coming eventually!

Generate the place file, open it in Roblox Studio, then run:

```sh
rojo serve
```

Connect to the running development server from within Roblox Studio. All your code should automatically sync in!

## License
This project is available under the terms of the Creative Commons CC0 license. Details are available in [LICENSE.txt](LICENSE.txt).