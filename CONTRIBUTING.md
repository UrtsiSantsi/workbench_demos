# Contributing

Thank you for considering contributing. Feel free to [get in touch](https://matrix.to/#/%23workbench:gnome.org).

## Getting started

1. [Install Workbench from Flathub](https://flathub.org/apps/re.sonny.Workbench)
2. Go through the Welcome Library entry

## Introduction

If you're completely new to GNOME development this is for you.

Open the "Welcome" example from Workbench Library.

Important fundamentals are

- objects
- properties
- signals

Every widget in GTK is an object. For example, `Gtk.Box`, `Gtk.Button`, ...

Properties affect an object to change its appearance or behavior.

Signals are events that can be listened to. Like `clicked` on `Gtk.Button`.

The Welcome example in the Library has all 3. Play with it, try to understand and make changes. If you break things you can always go back by select "Welcome" example from the Workbench Library again.

Once you understand these 3 things, try creating something new. There are plenty of widgets and patterns to explore.

## Setup

We provide a couple of tools to make the development process pleasant.

- Code formatter that runs automatically on git commit
- Single command to run all the tests locally

```sh
# Ubuntu requirements
# sudo apt install flatpak flatpak-builder nodejs make
# Fedora requirements
# sudo dnf install flatpak flatpak-builder nodejs make

cd demos
make setup
```

Before submitting a PR, we recommend running tests locally with

```sh
make test
```

## Contributing a new demo

Library entries have 3 functions

1. Showcase the capabilities of the platform
2. Teach how to use the APIs, patterns and widgets
3. Provide functional snippets ready to use

Pick a widget and make a Library demo for it within Workbench directly.

Check [here for ideas](https://github.com/workbenchdev/demos/issues/3).

Some guidelines

- Start with something small and accessible
- Focus on quality over quantity
- Make sure you don't pick something deprecated
- Select "Blueprint" instead of "XML" in the UI panel
- Keep it concise and interactive
- Add links to follow up on the topic covered
- Follow the patterns of existing entries
- Follow [the Style Guide](./STYLEGUIDE.md)

## Create Library entry

To create a new Library entry, duplicate an existing one and proceed to the next section.

```sh
cp -r demos/Button demos/Something
```

### Update Library entry

To update or port an existing Library entry

1. Open Workbench
2. Select "Open Project…" in the menu
3. Select the corresponding demo folder, for example `demos/Something`
4. Make the changes

## Submitting a contribution

Once you're satisfied with the result - you can send a pull request to include it in in this repository and Workbench.

Some guidelines:

- One pull request per Library entry
- Use a short PR title - eg. "Add Video entry" - it will be used as commit message
- If relevant, mention the related issue in the PR description
- Always review your own work before asking someone else

See also [the list of Library entries](https://github.com/workbenchdev/Workbench/wiki/Language-support-table) and some additional instructions on the Wiki.

## Learn

Here is a compilation of resources to learn more about the GNOME platform.

- [Workbench](https://github.com/workbenchdev/Workbench) 😉
- [GObject](https://gjs.guide/guides/gobject/basics.html#gobject-construction)
- [GTK4 + GJS Book](https://rmnvgr.gitlab.io/gtk4-gjs-book/)
- [Asynchronous programming](https://gjs.guide/guides/gjs/asynchronous-programming.html)
- [API references](https://gjs-docs.gnome.org/) make sure to enable at least GTK, GJS, GLib, Gio
- [GJS docs](https://gitlab.gnome.org/GNOME/gjs/-/tree/master/doc)
- [GJS examples](https://gitlab.gnome.org/GNOME/gjs/-/tree/master/examples)
- [Human Interface Guidelines](https://developer.gnome.org/hig/)
