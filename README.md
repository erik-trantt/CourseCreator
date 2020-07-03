# CourseCreator
This project is created and maintained by a team of 3, [@HarshilSiyani](https://github.com/HarshilSiyani), [@zachchung](https://github.com/zachchung) and [@erik-trantt](https://github.com/erik-trantt)(me). This repo is a fork from the [original repo](https://github.com/HarshilSiyani/CourseCreator).

What're new in this repo:
- additional work on code refactoring 
- UI/UX optimization

## Project aim
CourseCreator is a web app that help educators quickly transfer existing knowledge to digital format and share it with students. At this stage, the resources are lesson module and quiz module. 

- Quiz module has a quiz builder for quiz, questions and answers.
- Lesson module contains text, multimedia (e.g., image and videos) and reference link to external resources.

To create content on the website, we use a Trix text editor that is natively integrated into ActionText module of Ruby on Rails version 6.

## Challenges
1. Embedding videos using Trix editor
1. Nested form at 3-level depth for building quiz with multiple questions and answers

## Setup & Deployment
### Requirements
1. Ruby (version 2.6.6)
Use `ruby -v` to check your Ruby version on local machine.

2. Ruby gems:
`gem install rails rake bundler rspec rubocop rubocop-performance pry pry-byebug`
[Rails gem](https://guides.rubyonrails.org/v6.0/getting_started.html) is essential for this project.

3. PostgreSQL database:
```bash
# for macOS
brew install postgresql
brew services start postgresql

# for Ubuntu
sudo apt install -y postgresql postgresql-contrib libpq-dev build-essential
sudo -u postgres psql --command "CREATE ROLE `whoami` LOGIN createdb;"
```

### Setup
Clone the project, and run on local machine
```bash
git clone git@github.com:erik-trantt/CourseCreator.git
cd CourseCreator
bundle install
yarn install --check-files
```

Once the project is made available on your local machine, create the database in PostgreSQL and populate structure and data.
```bash
rails db:drop #=> only if you have the databases setup before
rails db:create
rails db:migrate
rails db:seed
```

### Deployment
Start the application with:
```bash
rails s
```

## Next steps
Sections to work on next addition:
- [x] Setup local development environment
- [ ] Tests
- [ ] Gems

