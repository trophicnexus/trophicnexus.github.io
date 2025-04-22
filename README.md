# Trophic Nexus - Website
Copyright (c) 2025, Joshua J. Hamilton  
Email: <josh@trophicnexus.com>  
URL: <https://www.linkedin.com/in/joshamilton/>  
URL: <https://trophicnexus.com>  
All rights reserved.

This repository contains the source code for my personal website, built using [Jekyll](https://jekyllrb.com/) and based on the [Freelancer Theme](https://github.com/jeromelachaud/freelancer-theme).

## Features

- Portfolio showcasing services
- Ability to add a grid of projects
- Contact form integration using [Formspree](http://formspree.io/)
- Responsive design

## Project Structure

The repository is organized as follows:

### Root Files
- **_config.yml**: The main configuration file for the Jekyll site. Update this file to change global settings, such as the site title, description, contact email, and color scheme.
- **index.html**: The main entry point for the site. This file includes the header, footer, and content sections.
- **style.css**: The main stylesheet for the site. Update this file to change the site's appearance.
- **.ruby-version**: Specifies the Ruby version required for the project.
- **Gemfile**, **freelancer-theme-jekyll.gemspec**, and **Gemfile.lock**: Define the Ruby gems required to build the site. Use `bundle install` to install dependencies.



### Key Directories

#### `_layouts/`
Contains layout templates for the site:
- **default.html**: The main layout file that includes all sections of the site.
- **styles.html**: Links to the CSS stylesheets used in the site.


#### `_includes/`
Contains reusable HTML snippets that are included in various parts of the site:
- **meta.html**: Contains metadata for the site, such as the title and description.
- **header.html**: Defines the navigation bar and site header.
- **trophicnexus.html**: Contains the introductory text for the site header.
- **about.html**: Defines the "About" section of the website, containing the headshot and bio.
- **projects.html**: Displays the grid of portfolio projects.
- **project-modals.html**: Defines the modal popups for project details.
- **services.html**: Displays the grid of services offered.
- **service-modals.html**: Defines modal popups for service details.
- **contact.html**: Defines the "Contact" section, including the contact form.
- **footer.html**: Contains the footer content, including copyright and social media links.
- **js.html**: Includes JavaScript files used across the site.

#### `_services/`
Contains Markdown files for individual services offered. Each file includes:
- `title`: The name of the service.
- `bullets`: A list of features or highlights for the service.

To add a new service, create a new Markdown file in this directory using the existing files as templates.

#### `_projects/`
Contains Markdown files for individual portfolio projects. Each file represents a project and includes metadata such as:
- `modal-id`: Unique identifier for the project modal.
- `img`: Image filename for the project thumbnail.
- `description`: A brief description of the project.

This section is not used by default. To enable it:
- `% include` the files `projects.html` and `project-modals.html` in the `default.html` file in the `_layouts/` directory.
- update the images in `img/projects` and modals in `_projects/`
- update the `project-modals.html` file to include the project modals.

To add a new project, create a new Markdown file in this directory using the existing files as templates.

#### `css/`, `img/`, `js/`
- **css/**: Contains custom stylesheets for the site.
- **img/**: Stores images used throughout the site, including project thumbnails and headshots.
- **js/**: Contains JavaScript files for interactive features.

#### `_site/`
The output directory where the built site is generated. Do not edit files in this directory directly, as they are overwritten during the build process.

### Updating the Website
- **Add Images**: Place new images in the `img/` directory.
- **Update Services**: Add or edit Markdown files in the `_services/` directory.
- **Update Projects**: Add or edit Markdown files in the `_projects/` directory.
- **Modify Sections**: Edit the corresponding files in the `_includes/` directory.


## Local Deployment

To build and serve the website locally, follow these steps:

1. Install Prerequisites:
    - Ensure Ruby 3.4.1 is installed (specified in .ruby-version).
    - Install Bundler:
    ```bash
    gem install bundler
    ```
    
2. Clone the Repository:
    ```bash
    git clone https://github.com/joshamilton/josh-trophicnexus.github.io.git
    cd josh-trophicnexus.github.io
    ```

3. Install Dependencies:
    ```bash
    bundle install
    ```

4. Build the Site:
    ```bash
    bundle exec jekyll build
    ```

5. Serve the Site Locally:
    ```bash
    bundle exec jekyll serve
    ```

The site will be available at http://localhost:4000.

## Production Deployment

## License
This project is licensed under the MIT License. See the LICENSE file for details.