# Omo Dapp Starter
Snowpack, Svelte, Typescript, Tailwind, Fission 

## Install

Clone Repo 
`git clone https://github.com/omoearth/omo-snowpack-svelte-typescript-tailwind-fission.git`

Enter directory 
```bash
cd omo-snowpack-svelte-typescript-tailwind-fission
```

Install with npm
```bash
npm i
```

Start
```bash
npm run dev
```
Go to your browser and open https://localhost:8080


### Building for production
The `build` script will compile the app for production. By default, the bundle will be created at `/public/build/`, which means your public directory will contain everything you need to run the app.

```bash
npm run build
```

### Hostless deployment to ipfs via fission
For more information about fission, read the docs: 
https://guide.fission.codes/

Install
```bash
brew install fission-suite/fission/fission-cli
```

Setup your account keys with fission
```bash
fission setup --verbose
```

Register your dapp and enter path of build folder (./public)
```bash
fission app register --verbose
```

Publish and delpoy your dapp
```bash
npm run deploy
```
This will first build and then publish your dapp to ipfs via the fission service
