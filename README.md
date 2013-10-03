# Rubyscholar

# Synopsis

Here is a small script to "scrape" your Google Scholar citations and reformat them (the way I need it for my website). 
Not super flexible - but should be easily customizable.

Some features: 

 * if registered on Crossref, retreives corresponding DOIs and can add altmetric.org links. 
   If Crossref doesn't think your email is valid, no DOIs will be retreived. 
 * adds "Cited by N" for popular papers

# How to use:

### As a Ruby Gem:
1. Install the gem using: `[sudo] gem install rubyscholar`
2. Create and configure a `config.yml` file.
      To create a `config.yml` file, run `$ rubyscholar init`
      Edit the file, filling in your details.
3. Run as `$ rubyscholar scrape --out file.html `.
4. A `file.html` file is created containing your citations all formatted
and ready to use.
5. Done!

### As a ruby script:
1. Configure "config.yml"
   If you want DOI retreival to work (including Altmetrics), you need to be 
   registered at crossref (its free). 
2. Run `ruby bin/scrape.rb` 
3. A scholar.html file is created with your publications from google scholar. 
4. Thats it. 

# Potential for improvement:

 * uses author list as visible on your main Google Scholar page. Sometimes this 
   means names are chopped in two or just a single author is missing. This could
   be made smarter. 
 * flexible output
 * flexible use of DOIs

# Technologies

Ruby, Nokogiri. Thanks to Google Scholar and Crossref. I hope none of this infringes on anything. 

# Contact

RubyScholar was developed by Yannick Wurm (http://yannick.poulet.org). Pull requests, patches and bug reports are welcome. The source code is available on github. Bug reports and feature requests may also be made there.

# Copyright

RubyScholar © 2013 by Yannick Wurm. Licensed under the MIT license. 

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
