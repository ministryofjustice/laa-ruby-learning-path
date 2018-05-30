## Learning Path for Ruby Programming

What follows is a list of resources collated into a ‘learning path’ for Developers to upskill in Ruby programming. 

Resources are laid out in steps which follow on from each other. However, it is not meant as a directive to follow exactly in the order laid out here. Similarly, there is no need to go trhough every resource mentioned here. Rather, this is intended as a guide to give you a bit of context as to what recource to look at as you develop more skills. 

The aim here is to give you a path you might take to structure your development as a Ruby programmer. If you’re not feeling some of the resources here then please feel free to replace / supplement them with things from elsewhere.

### Step 0: Prerequisites:
- UNIX/LINUX Command line – no need to master this, but it is pretty much a given in Ruby programming that you are familiar with this:
  - Pluralsight course on the Unix command line [here](https://app.pluralsight.com/library/courses/meet-command-line/table-of-contents)
  - Good and short [book](https://www.learnenough.com/command-line-tutorial) on this.
  - Git most of you should be familiar with this but for the uninitiated here is a [Pluralsight](https://www.pluralsight.com/courses/git-fundamentals) course – and here is a short [book](https://www.learnenough.com/git-tutorial) to get you started.
  - For extra points have a look at this course on [Test Driven Development](https://www.pluralsight.com/courses/test-driven-development-big-picture) (TDD)– you won’t be doing this straight away but it make sense to understand this mind-set from the beginning.

### Step 1: Installing Ruby:
- **WARNING:** OSX already has a version of Ruby installed – but beware - it is not advised that you rely on this version, as OSX uses it internally to organise things, so relying on it can be problematic.
  - Instead follow the steps here to install the Ruby version manager [rbenv](https://github.com/rbenv/rbenv#homebrew-on-macos).
  - Install ruby versions onto you Mac by following this [link](https://github.com/rbenv/rbenv#installing-ruby-versions).
  - Other version managers include [RVM](https://rvm.io/) and [chruby](https://github.com/postmodern/chruby).

### Step 2: Basic Ruby Programming:
- Very quick [tutorial](https://www.youtube.com/watch?v=Dji9ALCgfpM) to familiarise yourself with the basics of the language.
- Basic control flow, variables, data-structures on [Pluralsight](https://app.pluralsight.com/library/courses/ruby-fundamentals/table-of-contents).
- More on Object orientated ruby on [Pluralsight](https://app.pluralsight.com/library/courses/ruby-beyond-the-basics/table-of-contents).
- Book on the basics of ruby (has lots of good exercises in it) called [Learn Ruby the Hard Way](https://learnrubythehardway.org/book/).
- Great site to practice coding Ruby via code **‘katas’**, its called [codewars.com](https://www.codewars.com/).
- Alternative to codewars is [exercism.io](http://exercism.io/) which has a similar theme to codewars but it does not use an online IDE. 
- [IRB](http://ruby-doc.org/stdlib-2.0.0/libdoc/irb/rdoc/IRB.html) (_'interactive ruby'_) - this is a tool to interactively execute Ruby code in the command line. Type `irb` in the terminal after you have installed Ruby to activate this. It's very useful for testing small snippets of code in isolation.
- [slightly more advanced book](https://www.amazon.com/Practical-Object-Oriented-Design-Ruby-Addison-Wesley/dp/0321721330/ref=pd_sim_14_2?_encoding=UTF8&pd_rd_i=0321721330&pd_rd_r=2C15FQME1E5X744FGV1Z&pd_rd_w=h0K0z&pd_rd_wg=RqEfU&psc=1&refRID=2C15FQME1E5X744FGV1Z) which teaches you how to write robust Object Oriented ruby code. This is a highly recommened read as are all books by Sandy Metz on Ruby. You also might see this book refered to as POORD by the Ruby community. This is also a great book to read to improve your code in general.
- more lighthearted look at Ruby in this [book for Ruby beginners](https://poignant.guide/book/chapter-1.html).
- You might want to subscribe to the [Ruby Weekly](https://rubyweekly.com/) mailing list as a way to keep up-to-date with what's happening in the Ruby world. You'll get an email once a week with a few links to interesting articles on Ruby, Rails and related technologies.

### Step 3: Ruby Development Tools:
- Integrated Development Environments (IDEs) and Text editors – Pick one, I like [Visual Studio Code](https://code.visualstudio.com/), others include: 
  - [Ruby Mine IDE](https://www.jetbrains.com/ruby/) – this is a fully featured Ruby / Rails IDE with autocomplete etc. note this is not an open source product and requires a licence to use. But it does have a trial period.
  - [Atom](https://atom.io/) – an open source text editor built by github – has packages you can install that make Ruby programming easier
  - [Sublime Text 3](https://www.sublimetext.com/3) - this is another text editor that is widely use and as numerous plugins for Ruby development.
 
- Package management in Ruby is done with Ruby Gems.
  - Info on [what gems are and what you can do with them](https://guides.rubygems.org/what-is-a-gem/).
  - Pluralsight course on [creating your own Ruby gems](https://app.pluralsight.com/library/courses/building-ruby-gems/table-of-contents).
  - [click here](http://awesome-ruby.com/) for a collated directory of tools / gems for pretty much any use case you can think of. This is really cool and you should check it out.
  - [rubygems.com](https://rubygems.org/) is the main repository that bundler uses to install gem dependencies in projects. Most of the source code for these hosted on [github](https://github.com/).   
  - It would be good practice to create a simple Ruby Gem yourself to get a better understanding of how they work.
    - [This link](https://guides.rubygems.org/make-your-own-gem/) will guide you through the creation of a Gem. 
 
- [Bundler](https://bundler.io/) is used to manage dependencies, in conjunction with RubyGems (think Maven if you’re coming from a Java background, it uses Gemfiles which are the equivalent of a Maven pom.xml file). 
  - [Gems](https://en.wikipedia.org/wiki/RubyGems) are what Ruby packages are called (think .jars), they need to be installed and then ‘required’ into your project, in a similar fashion to Java imports.
  - bundler uses [`Gemfiles`](https://bundler.io/v1.5/gemfile.html) which allow you to declare your projects dependencies in an easy syntax. You can then install declared dependencies using `bundle install` on the command line in your project root.
  - Bundler also creates a [`Gemfile.lock`](https://bundler.io/v1.3/rationale.html#checking-your-code-into-version-control) snapshot file which declares the exact versions of dependencies that you know work for your application. This should be checked into source control along with your `Gemfile`.
  - [here is a more in-depth discussion](https://andre.arko.net/2015/04/28/how-does-bundler-work-anyway/) of what bundler is actually doing.
  - You can also use Bundler to simplify the creation of RubyGems, follow [this link](https://bundler.io/v1.12/guides/creating_gem.html) to find out more.
  - A note on using Bundler: gems installed by Bundler will affect gems you install using `gem install`. Bundler effectively creates a sandboxed environment. Using Bundler to manage Gems means that you shouldn't run into Gem version conflicts across projects as the Gems are localized to a given project.

- Documentation - Ruby is an extremely well documented language. Find the code language docs here:
  - Ruby [core library](https://ruby-doc.org/core-2.5.0/).
  - Ruby [standard library](https://ruby-doc.org/stdlib-2.5.0/) i.e. language features that are installed with your Ruby installation automatically but you still have to `require` into your programs.
  - Use the [RubyGems website](https://rubygems.org/) to find documentation on individual gems you’re using in your application.

- Debugging:
  - used [Pry](http://pryrepl.org/) which is a command line tool to perform debugging of ruby apps. It can also be used as an alternative to the 'IRB' in-line ruby runtime that comes as standard in ruby installations (see step 4 bullet-point 6). 
  - There are also integrations in text editors like [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby) and [Ruby Mine](https://www.jetbrains.com/help/ruby/debugging-code.html) which perform similar functions.
  - an alternative to Pry is [byebug](https://github.com/deivid-rodriguez/byebug).
 
- Build automation / task runners 
  - [Rake](https://ruby.github.io/rake/), short for _Ruby + make_ ([Make](https://en.wikipedia.org/wiki/Make_(software)) being a general build tool for [Unix](https://en.wikipedia.org/wiki/Unix) / [Unix-like](https://en.wikipedia.org/wiki/Unix-like) Operating Sysytems). 
  - Rake is a build automation tool that is used to perform tasks on code (e.g. things like [minifying](https://en.wikipedia.org/wiki/Minification_(programming)) Javascript or running automated tests). It is used heavily in the Rails frame work for things like database migrations. It might be best to look into this in the context of Rails (see step 3).
 
- Testing Frameworks:
  - Great course on testing Ruby / rails apps on Pluralsight [here](https://app.pluralsight.com/library/courses/test-driven-rails-rspec-capybara-cucumber/table-of-contents). This course is really good, I highly recommend this.
  - [Minitest](http://ruby-doc.org/stdlib-2.0.0/libdoc/minitest/rdoc/MiniTest.html) – default Ruby test framework which comes as part of it’s standard library (since Ruby 1.9).
  - [RSpec](http://rspec.info/) – the de-facto Ruby testing framework for TDD.
  - [factory_bot](https://github.com/thoughtbot/factory_bot) (Note: until fairly recently this was called _factory_girl_, it is referred to by this name in some of the resources). Can be used to mock objects to create test data in Ruby apps. More info [here](https://semaphoreci.com/community/tutorials/working-effectively-with-data-factories-using-factorybot).
  - [Cucumber](https://cucumber.io/) is a BDD ([Behaviour Driven Development](https://inviqa.com/blog/bdd-guide)) acceptance testing framework you can in conjunction with [Capybara](https://github.com/teamcapybara/capybara) (Think Selenium if you’re from Java) to run automated browser tests. Note: it can be used with selenium if needed see [here](https://github.com/teamcapybara/capybara#drivers). You set up [feature files](https://github.com/cucumber/cucumber/wiki/Feature-Introduction) using the ([Gherkin](https://github.com/cucumber/cucumber/wiki/Gherkin) Language) which describe journeys through you application and you then test your app against these. Introduction to this kind of testing [here](https://www.youtube.com/watch?v=lC0jzd8sGIA). Some tips on writing better feature files [here](http://www.bbc.co.uk/blogs/internet/entries/ff14236d-098a-3565-b678-ff4ba5776a5f).


### Step 4: Web frameworks / web programming:
- [Sinatra](http://sinatrarb.com/) this is a very lightweight web framework that is a good place to start for Ruby web programming.
  - Basic tutorial [here](https://www.sitepoint.com/just-do-it-learn-sinatra-i/)
  - More comprehensive on Sinatra book [here](http://sinatra-org-book.herokuapp.com/).
  - youtube [tutorial](https://www.youtube.com/watch?v=YIqEQW1alNw) on building a simple full stack web app in Sinatra.
  - Really good [book on Sinatra](https://www.amazon.co.uk/Jump-Start-Sinatra-Speed-Weekend-ebook/dp/B00TJ6UY8O/ref=sr_1_1?ie=UTF8&qid=1525193528&sr=8-1&keywords=Jump+Start+Sinatra&dpID=511OQH7nxGL&preST=_SX342_QL70_&dpSrc=srch), though you have to pay for it is very good, and I would recommend checking it out.
 
- [Ruby on Rails](https://rubyonrails.org/) (Rails for short) this is more of a ‘all bells and whistles’ web framework that allows you to develop web apps rapidly. It also has modules for things like [batch jobs](http://guides.rubyonrails.org/active_job_basics.html), [emails](http://guides.rubyonrails.org/action_mailer_basics.html) and [Restful APIs](http://edgeguides.rubyonrails.org/api_app.html).
  - Guide to Installing Rails [here](http://installrails.com/steps/configure_git).
  - Very good and free Rails [tutorial book](https://www.railstutorial.org/book).
  - [Pluralsight course](https://app.pluralsight.com/library/courses/ruby-rails-4-getting-started/table-of-contents) on Rails 4 (note this is on a slightly earlier version of Rails but the fundamentals are the same.)
  - Really good [Udemy course](https://www.udemy.com/professional-rails-5-development-course/) (Note have to pay about a £10 to access this course, google for a voucher as the quoted prices are far higher than what you actually need to pay).
  - A comprehensive book on Rails development in [Rails 5](https://pragprog.com/book/rails51/agile-web-development-with-rails-5-1)
 
- [Templating engines](https://en.wikipedia.org/wiki/Web_template_system ) which compile to HTML (basically JSP / JSF if you’re thinking in Java) can be used with Rails or Sinatra if you install the correct gems.
  - [Slim](http://slim-lang.com/)
  - [ERB](https://ruby-doc.org/stdlib-2.5.1/libdoc/erb/rdoc/ERB.html) (or embedded Ruby) – this is the default template engine in Rails/Ruby in general.
 
- [Rack](https://rack.github.io/) – this is the base package that almost all Ruby web frameworks are built around, it creates a common interface to allow Ruby frameworks to interact with webservers more easily. You might not need to know the ins and outs of this but if you’re interested here is a [Pluralsight](https://app.pluralsight.com/library/courses/ruby-building-web-apps-rack/table-of-contents) course that will teach you more about it and how it integrates with frameworks like Sinatra and Rails.

- Micro-services / apis:
  - [Grape](https://github.com/ruby-grape/grape) is a good choice to write microservices in Ruby it's a lightweight framework to write Ruby APIs, it's not as bare as Sinatra but it adds some useful features (especially params) without being as a heavyweight a framework as Rails.

### Step 5: supplementary tech:
- [Postgresql](https://www.postgresql.org/) is the main database used in production Ruby apps – [Pluralsight](https://app.pluralsight.com/library/courses/postgresql-getting-started/table-of-contents) course on this
[Setting up a Ruby on Rails on linux dev environment](https://app.pluralsight.com/library/courses/building-linux-server-for-ruby-on-rails/description).


### Step 6: More advanced books:
- The [rails 5 way](https://www.amazon.com/Rails-Way-Addison-Wesley-Professional-Ruby/dp/0134657675/ref=as_li_ss_tl?ie=UTF8&linkCode=sl1&tag=obiefernandez-20&linkId=5afcff9a3922096da60b0d03402052d5) – really in-depth look at Rails.
- Very comprehensive overview of Ruby language is the [Well Grounded Rubyist](https://www.amazon.com/Well-Grounded-Rubyist-David-Black/dp/1617291692/ref=pd_sim_14_6?_encoding=UTF8&pd_rd_i=1617291692&pd_rd_r=2C15FQME1E5X744FGV1Z&pd_rd_w=h0K0z&pd_rd_wg=RqEfU&psc=1&refRID=2C15FQME1E5X744FGV1Z)
- A great book on software [design patterns in Ruby](https://www.amazon.co.uk/Design-Patterns-Ruby-Russ-Olsen/dp/0321490452/ref=pd_sim_14_7?_encoding=UTF8&pd_rd_i=0321490452&pd_rd_r=2C15FQME1E5X744FGV1Z&pd_rd_w=h0K0z&pd_rd_wg=RqEfU&psc=1&refRID=2C15FQME1E5X744FGV1Z).

 

