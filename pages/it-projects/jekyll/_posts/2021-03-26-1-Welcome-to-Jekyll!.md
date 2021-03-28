---
# TODO: Layout für post in _layouts erstellen!
layout: page
title:  "Welcome to Jekyll!"
date:   2021-03-26 10:26
---
<div class="content">
  <img src="/assets/images/Jekyll/Welcome_to_Jekyll/jekyll_logo.png" alt="jekyll_logo" />
  <p>
    So let me introduce you to <a href="https://jekyllrb.com/">Jekyll</a> :) I want to talk about what it is, what it does for you and how to use it! In the upcoming articles I'll then take you with me on how I build this page using Jekyll and GitHub Pages.

    Jekyll is a command line tool that transforms simple Markdown, Liquid, HTML and CSS into static sites for your blog. No more databases you have to manage, comment moderation or annoying security updates, at least as long as you don't choose to add that stuff ;) It offers a lot of ways to customize your website by mostly using a simple folder structure and config file. You easily can  tweak the site's look and feel, URLs, data displayed, and more to you personal liking. It is easy to use with GitHub Pages which offers free static site hosting for you.

    There are some helpful sites like <a href="https://www.siteleaf.com/">Siteleaf</a> to make writing articles and customize your site a bit easier but I wanted to learn how Jekyll works so I decided to install it on my PC and go with the command line. So let's begin!
  </p>

  <h2>1. Installing Jekyll</h2>
  <p>
    <p>
      So installing Jekyll is pretty simple but Jekyll needs some prerequisites.

      <h3>Setup Ruby and RubyGems</h3>
      Because Jekyll is a RubyGem it needs Ruby and RubyGems and so you have to install these first. At the time I'm writing this post Jekyll requires Ruby version 2.4.0 or higher.
      If you don't have Ruby yet, just get it <a href="https://www.ruby-lang.org/en/downloads/">here</a>. Just make sure you get the version with the devkit. I am getting the latest version for <a href="https://rubyinstaller.org/downloads/">Windows</a> 64bit (currently 3.0.0).
      <br/><br/>
      While you go through the installation process, make sure you check the MSYS2 toolchain which contains the last requirements for Jekyll - GCC and Make.
      <img src="/assets/images/Jekyll/Welcome_to_Jekyll/install_msys2.jpg" alt="install msys2" /><br/>
      After that you get asked to install <code>ridk</code> with MSYS2 what you do. In the command prompt just hit enter and the installation should start. After that just hit enter again and you're done.
    </p>
    <p>
      Now that you have Ruby installed (you can check for succes with <code>ruby -v</code> in command line tool), you should check if RubyGems is installed as well by typing <code>gem -v</code>. If there is no version installed just follow the three simple steps <a href="https://rubygems.org/pages/download">here</a>.
    </p>

    <h3>Install Bundler and Jekyll</h3>
    <p>
      So to make sure all gems are installed properly with the required version you use <a href="https://bundler.io/v2.2/#getting-started">Bundler</a>. If you want to know more about Bundler and Gemfiles you can read about it in a small section at the bottom of the article.</br></br>
      <!-- TODO: Abschnitt verlinken mit Anker! -->
      To install bundler, which handles your gems for you, just open a command line tool and type <code>gem install bundler</code> and to install jekyll <code>gem install jekyll</code>.

      <img src="/assets/images/Jekyll/Welcome_to_Jekyll/install_bundler_jekyll.jpg" alt="install needed gems" />
      <br />
      You're done with the installation now! :)
    </p>
  </p>

  <h2>2. Init Jekyll - Let the fun part begin!</h2>
  <p>
    <p>
      Now that everything is ready to go, let's initialize our Jekyll site. <br/><br/>
      ***Quick note at this point: Some custom themes for Jekyll when using GitHub Pages (like the one I use) do not require initializing a Jekyll folder and instead just have to be forked. But more on that in the next article.***<br/><br/>
      Create your folder for Jekyll anywhere you want (but you might need admin rights at some point). Open your command line tool and navigate to that folder or (at least on Windows) you can type cmd in the folder path in your explorer. Now, to initialize your Jekyll blog, just type <code>jekyll new .</code>. This command creates everything for Jekyll in the current folder.

      <p style="color: red">
        Important note: I don't know why Jekyll doesn't install it by itself but to prevent errors (especially when it comes to previewing) you need to install the following gem as well with your command line: <code>gem install webrick</code>.
      </p>
    </p>

    <p>
      If you want to take a look at your page just open a command line tool in your jekyll folder and run <code>bundle exec jekyll serve</code>. Wait until it says <code>Server running...</code> and then open <code>localhost:4000/index.html</code> in your browser. To close the local server just press <code>STRG+C</code> (Windows) until it's not asking anything anymore.

      This should be your final folder structure now.<br />
      <img src="/assets/images/Jekyll/Welcome_to_Jekyll/final_folder_structure.jpg" />
    </p>
  </p>

  <h2>3. Nice to know: Gemfiles and Bundler</h2>
  <p>
    <h3>Gemfiles</h3>
    <p>
      So you might have noticed the Gemfile file (not the .locked). In these files you specify what gems you want to use for your Ruby application (your Jekyll website in this case). They'll be loaded for you without having to "require" them. <br /><br />
      A Gemfile usually looks like this:<br />
      <pre><code>
        ruby '3.0.0'

        gem "webrick", "~> 1.7"
      </code></pre>
      Bundler (and RubyGems since version 2.0) can red this file and then install all the requested versions of the listed gems. <br /></br>
      You might have noticed this weird symbols <code>~></code>. The symbols allow you to request a specific range of versions and in the case for webrick in says greater or equal version to 1.7.
    </p>
    <h3>Bundler</h3>
    <p>
      Bundler is, simply said, a dependency management tool. Besides RubyGems, which already handle this, it's not handling the versioning only for RubyGems but for your whole Ruby application! Just use <code>bundler update</code> in the folder with your Gemfile and Bundler is doing everything else.
    </p>
  </p>

  <h2>4. Soooooon...</h2>
  <p>
    So now you got a full working Jekyll installation :) In the next article I'll talk about GitHub Pages, Jekyll Themes and how to use everything together. Hope you enjoyed and stay healthy (I have an eye on you Corona..)!
  </p>

  <h2>Sources:</h2>
  <p>
    <a href="https://www.rubyguides.com/2018/09/ruby-gems-gemfiles-bundler/">RubyGuides</a><br/>
    <a href="https://bundler.io/v2.2/#getting-started">bundler.io</a><br/>
    <a href="https://jekyllrb.com/docs/">Jekyll Documentation</a><br/>
  </p>
</div>
