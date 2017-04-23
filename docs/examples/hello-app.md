## Angular CLI Hello APP

Lets's assume that you have followed the [install instructions](https://gitlab.com/exadra37-docker-images/angular-cli/blob/master/docs/how-to/install.md), therefore you should have this Repository installed in `~/Developer/Acme/Angular2/HelloApp`.


### STEP 1

Let's go to the folder where lives `docker-compose.yml`.

```bash
cd ~/Developer/Acme/Angular2/HelloApp/docker/angular-cli/src
```

### STEP 2

Lets' create a Docker Container with the Angular CLI with OhMyZsh shell from where we will invoke the Angular CLI or NPM commands.

```bash
sudo docker-compose run --rm --service-ports angular-cli
```

### STEP 3

We should be now inside our Docker Container with the awesome OhMyZsh shell, from where we have access to Angular CLI and NPM.

Let's create the HelloApp:

```bash
ng new HelloApp
```

### STEP 4

Moving inside the folder that has our new HelloApp:

```bash
cd cd HelloApp
```

### STEP 5

Now it's time to see it working on the browser.

```bash
ng serve --host 0.0.0.0
```

The output:

```bash
** NG Live Development Server is running on http://0.0.0.0:4200 **
Hash: 97d8054c07777655fa41
Time: 10164ms
chunk    {0} polyfills.bundle.js, polyfills.bundle.js.map (polyfills) 165 kB {4} [initial] [rendered]
chunk    {1} main.bundle.js, main.bundle.js.map (main) 3.62 kB {3} [initial] [rendered]
chunk    {2} styles.bundle.js, styles.bundle.js.map (styles) 9.77 kB {4} [initial] [rendered]
chunk    {3} vendor.bundle.js, vendor.bundle.js.map (vendor) 2.39 MB [initial] [rendered]
chunk    {4} inline.bundle.js, inline.bundle.js.map (inline) 0 bytes [entry] [rendered]
webpack: Compiled successfully.
```

### STEP 6

Now that WebPack already have compiled the HelloApp we can se it on the browser by visiting http://localhost:4200 .


### STEP 7

Play with the HelloApp and build something just for fun.

I hope you enjoy building Angular 2 Apps with a Docker Workflow.

If you like you may consider to [support further development](https://gitlab.com/exadra37-docker-images/angular-cli#support-development).


[HOME](https://gitlab.com/exadra37-docker-images/angular-cli)
