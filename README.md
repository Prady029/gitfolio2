# Gitfolio2
## **A spiced up version of @iamfunnee gitfolio repo with new additions.**
<img src="https://imgur.com/rMYrgku.png">

Gitfolio will help you get started with a portfolio website where you could showcase your work + a blog that will help you spread your ideas into real world.

Check out this [live demo](https://prady029.github.io) to see gitfolio in action.

# Getting Started

### Let's Install

Install gitfolio

```sh
npm i gitfolio -g
```

### Let's Build

GitFolio has a user interface you can use to customize your GitFolio page.  To begin using the UI, first run this command.

```sh
$ gitfolio ui

>Starting...
>The GUI is running on port 3000, Navigate to http://localhost:3000 in your browser
```
In your browser, browse to the address to begin configuring your page.

> Tip: You can use ui to create new blogs and for updating your folio too.

#### Using the command line

You can also create your GitFolio page automatically by providing your GitHub user name in command line mode.

```sh
gitfolio build <username>
```

`<username>` is your username on github. This will build your website using your GitHub username and put it in the `/dist` folder.

To run your website use `run` command, Default port is 3000

```sh
gitfolio run -p [port]
```

🎉 Congrats, you just made yourself a personal website!

### Let's Customize

#### Forks

To include forks on your personal website just provide `-f` or `--fork` argument while building

```sh
$ gitfolio build <username> -f
```

#### Sorting Repos

To sort repos provide `--sort [sortBy]` argument while building. Where `[sortBy]` can be `star`, `created`, `updated`, `pushed`,`full_name`. Default: `created`

```sh
$ gitfolio build <username> --sort star
```

#### Ordering Repos

To order the sorted repos provide `--order [orderBy]` argument while building. Where `[orderBy]` can be `asc` or `desc`. Default: `asc`

```sh
$ gitfolio build <username> --sort star --order desc
```

#### Customize Themes

Themes are specified using the `--theme [theme-name]` flag when running the `build` command. The available themes are

- `dracula`
- `dark`
- `light` (has been depreciated from ui, but availablr using terminal)

> TODO: Add more themes

For example, the following command will build the website with the dark theme

```sh
$ gitfolio build <username> --theme dark
```

#### Customize background image

To customize the background image just provide `--background [url]` argument while building.
I recommend,[unsplash](https://www.unsplash.com)

```sh
$ gitfolio build <username> --background https://images.unsplash.com/photo-1557277770-baf0ca74f908?w=1634
```

You could also add in your custom CSS inside `index.css` to give it a more personal feel.

#### Add Social Media links on your profile

Twitter, LinkedIn, Medium, Email, and Telegram links to your profile while building.

```sh
gitfolio build <username> --twitter <twitter_username> --linkedin <linkedin_username> --medium <medium_username> --email <email address> --telegram <telegram username>
```

#### Add your resume link on your profile

You can link your resume to your profile while building.

```sh
gitfolio build <username> --resume <resume link>
```

### Let's Publish

Head over to GitHub and create a new repository named `username.github.io`, where username is your username. Push the files inside`/dist` folder to repo you just created.

Go To `username.github.io` your site should be up!!

### Updating

To update your info, simply run

```sh
$ gitfolio update
```

or use the `Update` options in gitfolio's UI

This will update your info and your repository info.

To Update background or theme you need to run `build` command again.

### Add a Blog

To add your first blog use the UI.

```sh
$ gitfolio ui
```

This will open up a UI page and you can click on `New Blog` to create a new blog. Once you are done writing your blog you can hit the `Create Blog`.

This will create a blog inside `./dist/blog` folder.

Look for success or error in your terminal.

This also adds content to `blog.json` file. This file helps in showcasing your blogs on your personal website as [cards](https://imfunniee.github.io/gitfolio/#blog_section). You could customize the JSON object that corresponds your current blog.

[Click here](https://prady029.github.io/blog/) to see a Demo of the Blog feature in action.


