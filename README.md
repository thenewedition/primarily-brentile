## 📖 Installation

### Install Official Release

This option will give you access to public releases.

1. Open up Obsidian and go to Settings.
2. Inside Settings, head over to the Appearance tab.
3. Under Themes, you should find a button called, `Manage`. Click on it. This will open up the Community Themes page.
4. On the search bar, type `Primary`, and click the one that says, `By Cecilia May`. It should open up the theme.
5. Click `Install and Use` to install the theme! Enjoy.

### Install Beta Version

This option is exclusive to monthly subscribers of Primary.

1. Head on over to [Primary's Ko-fi](https://ko-fi.com/ceciliamay) page.Under Buy a Coffee, choose Membership and subscribe to get access to member exclusive posts.
2. After subscribing, head over to the `Posts` tab. This is under the header, just below my name and ko-fi link.
3. Once in the Posts tab, you should be able to find posts usually titled along the lines of `Primary x.x.x-beta (Monthly Subscriber Exclusive)`. Click on the latest post.
4. The post includes the full Release Notes so you're fully informed what new features or fixes you get for that release! To get the a copy of that beta, scroll down a bit until you find the `Click here to download the CSS file.` link. This should take you to a GitHub gist page.
5. On the GitHub gist page at the top right side, click **Download Zip**. This will give you a `.zip` file with 1 file inside, the `primary-x.x.x-beta.css` file (where x.x.x is the version number).
6. Unzip the file and copy the CSS file.
7. Paste it under your vault's `.obsidian/themes` folder. You can open this folder through Obsidian. To do so, open up *Settings*, and go to the *Appearance* tab. Under `Themes`, there's an icon beside the theme dropdown. Click it to open the themes folder. It should open up the folder `Vault Name/.obsidian/themes`. Paste the CSS file there.
8. Go back to Obsidian and open up your Command Palette. Type `Reload app without saving` and press enter so that your Obsidian gets reloaded and ensures it identifies the CSS file.
9. Once your Obsidian has reloaded, open up Settings -> Appearance tab. Under the `Themes` dropdown, select the `primary-x.x.x-beta` you downloaded. This should load the theme.
10. Reload the app again for best results.

### Developers

#### Build Instructions

Let's start by installing the essentials.

Primary is written with a mix of CSS and [Sass](https://sass-lang.com/guide/). If you haven't, do install Sass.

```
sudo gem install sass
```

After that, we need to install [GruntJS](https://gruntjs.com/configuring-tasks). Grunt allows developers to run various tasks that would otherwise be tedious. In our case, we want our repo to follow Obisidan's repository guidelines while making it easy for us to debug.

Prerequisites would be installing any [NodeJS](https://nodejs.org/en/download/package-manager/current) version.

```
npm install -g grunt-cli
```

#### Setting up your Theme Dev Environment

Within the repo's path, run `npm install` to build all the necessary modules.

Then, go to the `.env.example` and **define your local Obsidian vault path**.

Update the `OBSIDIAN_PATH` to the local path of your Obsidian theme folder.

Once done, rename the file from `.env.example` to `.env`.

#### Code, Build and Test

Run the command below when you start writing code and testing.

```
npx grunt
```

> [!NOTE] What does the command do?
> The command activates the grunt file so that when you save a file in the repo, the Grunt file watches for your save, compiles the CSS and Sass files, minifies it, and copies it in to two locations — one into this repository, and one into the defined path in the `.env` file. This ensures we have an identical copy for testing live within your vault, and one ready for publishing!


