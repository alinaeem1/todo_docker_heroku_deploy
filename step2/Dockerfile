FROM nginx:alpine

LABEL author="Waqas"
LABEL containerizer="Muhammad Waqas"
# I have tested different directories, but those does not work
# It's mandatory to mention the same directory to copy html files.
# Override the default config of nginix to use our own settings
COPY default.conf /etc/nginx/conf.d/default.conf
# Copy files to our image
COPY . /usr/share/nginx/html
# Override default command
CMD sed -i -e 's/$PORT/'"$PORT"'/g' /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'