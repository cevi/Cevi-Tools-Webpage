# Create a new Blog Post

You can create a new blog post by creating a markdown file with a name in the form `YYYY-MM-DD-blog_title.md` in this
directory. Please make sure that you have included the following snipped at the top of your Markdown file. The authors will be parsed and the link to their github account will be automatically inserted.

```markdown
---
layout: post
title:  "Thats your Blog Title"
date:   2021-11-25 12:55:00 +0100 # That's the release date of the blog entry
categories: some_category
authors:
 - github@author1_github_nick Author 1 Name
 - Author 2
---

Your blog content as normal Markdown text.

```

For projects (tools):

```markdown
---
layout: tool
title:  "Tool Title"
date:   2021-11-25 12:55:00 +0100 # That's the release date of the blog entry
categories: [tool, tool-ready-to-use]
image: assets/tools-frontpage/cevi_logo_generator.jpg
deployment: https://logo.cevi.ch
excerpt: This is the excerpt that will be displayed on the tools overview page.
authors:
 - github@author1_github_nick Author 1 Name
 - Author 2
---

Your blog content as normal Markdown text.

```

