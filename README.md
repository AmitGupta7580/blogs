# Peronal Blogs

<a href="http://blogs.ammmy.me">Blog Website</a>

This website is made with the use of `jekyll`.
Inspiration of Jekyll-Theme is taken from <a href="https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll">here</a>

## Code Description

1. Create the following pages if they do not exist already (or change the extension of existing markdown files from `.md` to `.html`):

   * `index.html` - set to `layout: page`
   * `about.html` - set to `layout: page`
   * `contact.html` - set to `layout: page`

2. Configure the `index.html` front matter. Example:

    ```markdown
    ---
    layout: home
    background: '/PATH_TO_IMAGE'
    ---
    ```

3. Configure the `about.html`, `contact.html`, and `posts/index.html` front matter. Example:

    ```markdown
    ---
    layout: page
    title: Page Title
    description: This is the page description.
    background: '/PATH_TO_IMAGE'
    ---
    ```

4. For each post in the `_posts` directory, update the front matter. Example:

    ```markdown
    ---
    layout: post
    title: "Post Title"
    subtitle: "This is the post subtitle."
    date: YYYY-MM-DD HH:MM:SS
    background: '/PATH_TO_IMAGE'
    ---
    ```

    For reference, look at the [demo repository](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll) to see how the files are set up.

5. Add the form to the `contact.html` page. Add the following code to your `contact.html` page:

    ```html
    <form name="sentMessage" id="contactForm" novalidate>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Name</label>
          <input type="text" class="form-control" placeholder="Name" id="name" required data-validation-required-message="Please enter your name.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Email Address</label>
          <input type="email" class="form-control" placeholder="Email Address" id="email" required data-validation-required-message="Please enter your email address.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
          <label>Phone Number</label>
          <input type="tel" class="form-control" placeholder="Phone Number" id="phone" required data-validation-required-message="Please enter your phone number.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Message</label>
          <textarea rows="5" class="form-control" placeholder="Message" id="message" required data-validation-required-message="Please enter a message."></textarea>
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <br>
      <div id="success"></div>
      <div class="form-group">
        <button type="submit" class="btn btn-primary" id="sendMessageButton">Send</button>
      </div>
    </form>
    ```

    Make sure you have the `email` setting in your `_config.yml` file set to a working email address! Once this is set, fill out the form and then check your email, verify the email address using the link sent to you by Formspree, and then the form will be working!

6. Build your site: `bundle exec jekyll serve`
