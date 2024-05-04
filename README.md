- 💕 Hi, I’m @arzoopatra
- 🏫 I’m B.Tech ECE Student at IGDTUW'27
- 🌱 I’m currently learning C & C++

<!---
arzoopatra/arzoopatra is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
name: Latest blog post workflow
on: 
    schedule:
        - cron: '0 * * * *'
jobs: 
    update-readme-with-blog: 
        name: Update this repo's README with latest blog posts
        runs-on: ubuntu-latest
        steps: 
            - uses: actions/checkout@v2
            - uses: gautamkrishnar/blog-post-workflow@master
              with: 
                max_post_count: "4"
                feed_list: "https://medium.com/feed/@dear_arzoo"
