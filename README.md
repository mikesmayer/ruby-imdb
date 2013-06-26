Welcome to Ruby IMDB
--------------------

ruby-imdb is IMDB parsing library for Ruby.

Features
--------

- Object Oriented design
- Fast access to data

Using in Gemfile
--------

- add the following code to your Gemfile: `gem 'ruby-imdb', github: 'tibbon/ruby-imdb'`
- run `bundle install` from the bash prompt


Usage
-----
    require 'rubygems'
    require 'imdb'

    s = IMDB::Search.new
    s.movie("fear and loathing in las vegas").each do |result|
      movie = IMDB::Movie.new(result.id)
      p movie.title
      movie.cast.each do
        |cast|
        p "#{cast.name} as #{cast.char}"
      end
      p movie.poster
    end

    movie = IMDB::Movie.new('0120669')
    p movie.poster


Authors
-------
- Yalcin ACIKYILDIZ (mailto:yalcin@webliyacelebi.com)
- Edited README.md by David Fisher/tibbon

This library is released under the terms of the GNU/GPL.

