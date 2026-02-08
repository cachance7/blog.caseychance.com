+++
title = 'Building a Dev Diary CLI Tool'
date = 2024-02-08T00:53:15-08:00
description = 'Creating a Rust CLI to manage and publish development diary entries to Hugo'
tags = ['rust', 'cli', 'hugo', 'productivity']
draft = false
+++

Today I built a command-line tool to streamline my development diary workflow. 
The tool manages entries in YAML format and publishes them to my Hugo blog with a single command.


## Motivation

I wanted a way to easily write development diary entries without manually managing Hugo's frontmatter format.

The goal was to keep entries in a structured YAML format that's easy to edit and version control.

Publishing should be as simple as running a single command.

## Implementation

Built with Rust using `clap` for the CLI, `serde_yaml` for parsing, and `chrono` for dates.

Entries are stored in the `entries/` directory and can be listed in reverse chronological order.

The `publish` command converts YAML entries to Hugo markdown and copies them to the blog repository.

## Features

**Create**: Generate new entries with a title and open them in your editor

**List**: View all entries with their status (published/draft), date, and description

**Publish**: Convert to Hugo format, validate, and deploy to the blog

**Edit**: Quickly open existing entries for modification

---

Now I can focus on writing instead of wrestling with YAML frontmatter! 🎉
