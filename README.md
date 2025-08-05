# Unity Profile Dev Site

A local Drupal 10 development site using the [Unity Profile](https://github.com/NCAR/unity-profile), built for testing, development, and configuration of NCAR's Unity-based upstream.

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

## Setup Instructions

```bash
# 1. Clone this repository (with submodules)
git clone --recurse-submodules https://github.com/NCAR/unity-profile-dev-site/
cd unity-profile-dev-site

# 2. Start DDEV
ddev start

# 3. Install PHP dependencies
ddev composer install

# 4. Install Drupal site (you may use the browser for full profile config)
ddev drush site:install unity_profile --account-name=admin --account-pass=admin

# 5. Launch the site
ddev launch

# 6. Develop in Unity Profile directory
cd web/profiles/custom/unity-profile
```

## To check whether the code follows the [Drupal coding standards](https://www.drupal.org/docs/develop/standards), run the following command from the project root:


```bash
ddev exec vendor/bin/phpcs --standard=Drupal web/profiles/custom/unity-profile/modules/opensky_publications
```

## Auto-fix fixable violations:

```bash
ddev exec vendor/bin/phpcbf --standard=Drupal web/profiles/custom/unity-profile/modules/opensky_publications
```

