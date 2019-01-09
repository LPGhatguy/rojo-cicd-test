# Rojo CI/CD Test
This project tests automatic deployment of Roblox places from GitHub. It demonstrates a complete CI/CD (continuous integration/deployment) pipeline like those elsewhere in the software industry.

Every commit to `master` will be deployed to [a place on Roblox.com](https://www.roblox.com/games/2726230850/CI-CD-Debugging) within a minute or two. The place file is generated and uploaded by [Rojo](https://github.com/LPGhatguy/rojo) only if tests pass.

This project be updated as features and improvements are made to the involved tools.

Tools:
* [Rojo](https://github.com/LPGhatguy/rojo) `master`
* [Lemur](https://github.com/LPGhatguy/lemur)
* Travis-CI

## Usage
You'll need the latest `master` of Rojo installed. You can do that by cloning the Rojo repository somewhere and using `cargo install`:

```sh
git clone https://github.com/LPGhatguy/rojo.git
cargo install --path rojo/server
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
Install the Rojo plugin from the `master` branch. Docs for how to do this easily are coming eventually!

Generate the place file, open it in Roblox Studio, then run:

```sh
rojo serve
```

Connect to the running development server from within Roblox Studio. Your project should automatically update as changes are made to files.

## License
This project is available under the terms of the Creative Commons CC0 license. Details are available in [LICENSE.txt](LICENSE.txt).