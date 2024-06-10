# Neurotech-Wiki
This is a wiki spun up using Rust's mdbook package. The aim is to make contributing and using the wiki as easy as possible. Deployment of the wiki is done using Netlify, any changes to this repository will be live on this [link](https://neurotechwiki.netlify.app).

# How to make changes to the wiki?

It is very simple! mdbook allows for markdown files to be rendered as static html pages. This means that if you want to add new content to the website and share it with the world, you can do so by just writing markdown. Lets focus on the directory that will be of your main concern `./src`.

`./src` contains the following files and directories: 

```bash
src
├── SUMMARY.md
├── eeg_data_processing
├── home.md
├── learning_resources
├── lecture_workshops
├── past_projects
└── python
```

`home.md` contains the content for your home page, consider this the first thing that the user sees when they first arrive on the website. 

### Updating the appendix

`SUMMARY.md` will contain the appendix which will correspond to contents within the sidebar. Sections are bulleted elements and subsections are indented by one tab like so:

```markdown
- [Home](./home.md)
- [Python Basics](./python/basics.md)
- [EEG Data Processing](./eeg_data_processing/signal_processing.md)
  - [Signal Processing Pipeline](./eeg_data_processing/signal_processing_1.md)
  - [Data Processing](./eeg_data_processing/signal_processing_2.md)
```

This will render to:

<img width="295" alt="image" src="https://github.com/Neurotech-Davis/Neurotech-Wiki/assets/87293108/e3421dca-c52f-4503-8707-761b6dce4252">

The name of the appendix entry is always followed by the relative path to the markdown file that you want to render. ex. `./python/basics.md`

### Adding content

Each section within the website has it's own dedicated directory which contain the markdown files that correspond to that sections, they can also be subsections. For example this is what the `past_projects` directory looks like:

```bash
src/past_projects
├── dinogame.md
├── hapticfeedback.md
├── intro.md
├── p300oddball.md
├── stressdetection.md
└── vrbasketball.md
```

If you want to add content to this section all you have to do is add a new markdown file to this directory and then link it in `SUMMARY.md`. If the topic you are adding is logically different then add another folder and name it appropriately in order to keep organization of the project simple.

After you have made the desired changes make sure to push them to the `main` branch of this repository, only then the changes will be live on the website. If you don't have access permission to the repository just create a fork and make your changes. Once you are done with your changes open a pull request and a neurotech board member will review and merge your changes.

### Deploying/Testing locally

You will need `cargo` installed on your computer. Cargo is a package manager and a build tool for Rust. Follow the instructions [here](https://doc.rust-lang.org/cargo/getting-started/installation.html) to install cargo. 

Assuming you have cargo installed you will need to install mdbook using this command:
```
cargo install mdbook

```

and that's it! you can now deploy locally using the following command:

```
mdbook serve --open
```

# Issues
If there are any issues with mdbook, please refer to the [docs](https://rust-lang.github.io/mdBook/index.html)

Please contact the author if there are any issues when deploying or if format goes bad.

Author: [Dhruv Sangamwar](https://github.com/dhruvsangamwar)

