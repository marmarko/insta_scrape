[![Build Status](https://travis-ci.org/dannyvassallo/insta_scrape.svg?branch=master)](https://travis-ci.org/dannyvassallo/insta_scrape)[![Gem Version](https://badge.fury.io/rb/insta_scrape.svg)](https://badge.fury.io/rb/insta_scrape)![](http://ruby-gem-downloads-badge.herokuapp.com/insta_scrape?type=total&color=brightgreen)

![alt text](https://s3-us-west-2.amazonaws.com/instascrape/instascrapelogo.png "logo")
# InstaScrape

The instagram swiss army knife. Restores all deprecated hashtag functionality and grants public api access from instagram's front end without any of the authorization.

#### Note [ *PLEASE READ* ]

The number of results may vary when using certain methods as this *IS NOT* an official endpoint.

## Installation

Add this line to your application's Gemfile:

```ruby
gem "insta_scrape"
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install insta_scrape

## How To Use

You'll probably want to use the [whenever](https://github.com/javan/whenever) gem or something similar in order to create hashtag widgets like you once could. Scheduling a job (polling) and storing each post's information in your database/cache is one way to do it.

*Basic Example(s)*
```ruby
#basic use case

#scrape_result = InstaScrape.user_info_and_posts("foofighters").posts
#scrape_result = InstaScrape.user_posts("foofighters")
scrape_result = InstaScrape.hashtag("test")
scrape_result.each do |post|
  puts post.image
  puts post.link
  puts post.text
end
```

See the InstaScrape Wiki [HERE](https://github.com/dannyvassallo/insta_scrape/wiki/) to learn the rest of InstaScrape's features.

## Problems? Need Help?

Create an [issue](https://github.com/dannyvassallo/insta_scrape/issues) and I'll respond as soon as I can. If it's a feature request and you've got some free time -- PRs are gladly welcomed.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/dannyvassallo/insta_scrape. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
