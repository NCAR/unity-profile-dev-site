# Unity Profile Dev Site

A local Drupal 10 development site using the [Unity install profile](https://github.com/NCAR/unity-profile), built for testing, development, and configuration of NCAR's Unity-based upstream.

Created by **Zongyao Yang**

---

## Quick Start

### Prerequisites

Ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [DDEV](https://ddev.readthedocs.io/en/stable/)
- [Composer](https://getcomposer.org/)
- PHP ≥ 8.1
- Git (with SSH or HTTPS access to GitHub)
- Access to the [Unity Profile repo](https://github.com/NCAR/unity-profile)

---

## 🛠️ Setup Instructions

```bash
# 1. Clone this repository (with submodules)
git clone --recurse-submodules git@github.com:NCAR/unity-profile-dev-site.git
cd unity-profile-dev-site

# 2. Start DDEV
ddev start

# 3. Install PHP dependencies
ddev composer install

# 4. Install Drupal site (you may use the browser for full profile config)
ddev drush site:install unity_profile --account-name=admin --account-pass=admin

# 5. Launch the site
ddev launch
