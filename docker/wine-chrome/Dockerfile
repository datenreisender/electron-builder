ARG IMAGE_VERSION=wine
FROM --platform=linux/x86_64 electronuserland/builder:$IMAGE_VERSION

RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - && \
  echo "deb http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google.list && \
  apt-get -qq update -y && \
  apt-get -qq install -y --no-install-recommends xvfb google-chrome-stable libgconf-2-4 && \
  # clean
  apt-get clean && rm -rf /var/lib/apt/lists/*