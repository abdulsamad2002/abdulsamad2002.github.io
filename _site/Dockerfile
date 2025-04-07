# Use the official Ruby image as the base
FROM ruby:3.2

# Install Jekyll and dependencies
RUN gem install jekyll bundler

# Set the working directory
WORKDIR /site

# Copy the Gemfile and Gemfile.lock (if they exist)
COPY Gemfile* ./

# Install Ruby gems
RUN bundle install

# Copy the rest of the site files
COPY . .

# Expose the default Jekyll port
EXPOSE 4000

# Command to serve the site
CMD ["bundle", "exec", "jekyll", "serve", "--host", "0.0.0.0"]