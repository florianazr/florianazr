- š Hi, Iām @florianazr
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
florianazr/florianazr is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
bot = TikTokBot()

# getting your feed (list of posts)
my_feed = bot.list_for_you_feed(count=25)

popular_posts = [post for post in my_feed if post.statistics.play_count > 1_000_000]

# extract video urls without watermark (every post has helpers)
urls = [post.video_url_without_watermark for post in popular_posts]

# searching videos by hashtag name
posts = bot.search_posts_by_hashtag("cat", count=50)
