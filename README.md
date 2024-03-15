# publisher

Monorepo was developed to solve hell and uncontrollable package contents in the simplest way possible. 

The goal of the project is simple. It will store the packages you send to the "publisher" in a specific directory and with a single command it will "publish" the "output" directory of the project as the main directory. You can also speed up your work by adding the output directory to your local projects.


## How to use it?
Add the configuration file to the project root with the following command.
```bash
  npx publisher repo-conf init
```
This command inserts a json with the following configurations
```json
{
  "name":"...",
  "project":"...",
  "tsconfig":"..."
}
```
Run the following command in the project directory so that the "publisher" updates itself as the "output" directory is updated. Actually I can do this with listeners, but why overuse your cpu :D ?
```bash
npx publisher sync
// or
npx publisher sync all
```

## How do I publish my project?

```bash
npx publisher publish-all
// or
npx publisher publish @my/repo
```
