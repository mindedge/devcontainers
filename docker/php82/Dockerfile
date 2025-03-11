FROM ubuntu:24.04 AS base
# Update system, install required tools, PHP, and Composer
RUN apt-get update -y && \
  apt-get install -y software-properties-common lsb-release curl unzip sqlite3 git && \
  add-apt-repository ppa:ondrej/php -y && \
  apt-get update -y && \
  apt-get install -y php8.2 php8.2-cli php8.2-fpm php8.2-common \
      php8.2-bcmath php8.2-bz2 php8.2-curl php8.2-dba php8.2-intl php8.2-mbstring \
      php8.2-mysql php8.2-readline php8.2-soap php8.2-xml php8.2-pgsql \
      php8.2-zip php8.2-sqlite3 php8.2-gd php8.2-soap && \
  curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

# Set the default command
CMD ["php", "-a"]