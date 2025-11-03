# ![Setup](../assets/hero-setup.png)

## Create and Clone Your Repo

Open your Terminal application and navigate to your `~/code/ga/lectures` directory:

```bash
cd ~/code/ga/lectures
```

Make a new repository on [GitHub](https://github.com/) named `men-stack-crud-app-fruits`.

Clone a copy of your remote repo locally by using the `git clone` command:

```bash
git clone https://github.com/<your-username>/men-stack-crud-app-fruits.git
```

> 🚨 Do not copy the above command. It will not work. Your GitHub username will replace `<github-username>` (including the `<` and `>`) in the URL above.

Next, `cd` into your new cloned directory, `men-stack-crud-app-fruits`:

```bash
cd men-stack-crud-app-fruits
```

## Initialize a Node Project

In this directory create a `server.js` file:

```bash
touch server.js
```

Create a node project along with its `package.json` file by using this command:

```bash
npm init -y
```

> The -y flag automatically accepts all default options (you can edit them later in package.json if needed).

Open the project directory in VS Code:

```bash
code .
```

---

<div align="center">

### Next Up 👉

[**Build and Run `server.js`**](./build-and-run-serverjs.md)

</div>

---
