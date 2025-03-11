FROM ubuntu:24.04 AS base
# Update system, install required tools, PHP, and Composer
RUN apt-get update -y && \
  apt-get install -y software-properties-common lsb-release curl unzip sqlite3 git && \
  add-apt-repository ppa:ondrej/php -y && \
  apt-get update -y && \
  apt-get install -y php8.1 php8.1-cli php8.1-fpm php8.1-common \
      php8.1-bcmath php8.1-bz2 php8.1-curl php8.1-dba php8.1-intl php8.1-mbstring \
      php8.1-mysql php8.1-readline php8.1-soap php8.1-xml php8.1-pgsql \
      php8.1-zip php8.1-sqlite3 php8.1-gd php8.1-soap && \
  curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

# Set the default command
CMD ["php", "-a"]