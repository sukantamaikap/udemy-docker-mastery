FROM drupal:8.2

RUN apt-get update && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

# go to theme folder
WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# change back to drupal home directory
WORKDIR /var/www/html