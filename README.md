# threagile-playground
This is a playground project for playing with Threagile.

## How to use 

- Set an alias to the Threagile Docker container (you need to have Docker installed) and mount it:

```console
# On Mac
alias threagile='docker run --rm -it -v $(pwd)/:/app/work threagile/threagile'
```

- Get IDE supporting files (if desired):

```console
threagile -create-editing-support -output /app/work
```

-  Create a target folders (if not yet existing):

```console
mkdir target
```

- Render the model:

```console
threagile -model /app/work/threagile.yaml -output /app/work/target
```

- Explore the resulting files in `./target` folder