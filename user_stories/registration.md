Github returns Monalisa's dataset

    {
      "login": "octocat",
      "id": 1,
      "avatar_url": "https://github.com/images/error/octocat_happy.gif",
      "gravatar_id": "",
      "url": "https://api.github.com/users/octocat",
      "html_url": "https://github.com/octocat",
      "followers_url": "https://api.github.com/users/octocat/followers",
      "following_url": "https://api.github.com/users/octocat/following{/other_user}",
      "gists_url": "https://api.github.com/users/octocat/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/octocat/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/octocat/subscriptions",
      "organizations_url": "https://api.github.com/users/octocat/orgs",
      "repos_url": "https://api.github.com/users/octocat/repos",
      "events_url": "https://api.github.com/users/octocat/events{/privacy}",
      "received_events_url": "https://api.github.com/users/octocat/received_events",
      "type": "User",
      "site_admin": false,
      "name": "monalisa octocat",
      "company": "GitHub",
      "blog": "https://github.com/blog",
      "location": "San Francisco",
      "email": "octocat@github.com",
      "hireable": false,
      "bio": "There once was...",
      "public_repos": 2,
      "public_gists": 1,
      "followers": 20,
      "following": 0,
      "created_at": "2008-01-14T04:33:35Z",
      "updated_at": "2008-01-14T04:33:35Z",
      "total_private_repos": 100,
      "owned_private_repos": 100,
      "private_gists": 81,
      "disk_usage": 10000,
      "collaborators": 8,
      "plan": {
        "name": "Medium",
        "space": 400,
        "private_repos": 20,
        "collaborators": 0
      }
    }

If the _octocat_ username has not been used yet it will be proposed to the user as DevTeamUp username. In any case the user has the possibility to change username at the registration time.

Same approach for the user's email.

The registration form also shows some other user's attribute like:

* spoken (human) languages
* default (human) language (mandatory)
* current timezone

Users are saved in a mongo database handled by the DevBook application

The github dataset is saved in the _githosts->github_ subtree of the user.

In the future other _githosts_ can be added in the same way.

The data retruned by github will be kept updated and will be used to elaborate user's metrics.


## Questions

Do we all agree on saving data and keep them updated or do you prefer to perform an API query every time?