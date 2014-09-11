# PR stats

This small tool shows a small statistic over configured repositories.
When the url http://localhost:8002/repo/{repository} gets opened the github will be queried to get data about all open PRs.
The data will be stored in the configured `prLog/{repository}` directory and displayed in the stats.

#### [Why, How and What: Read here!](https://github.com/dazz/repo-pr-stats/blob/master/doc/why-what-how.md)

### Run

* clone me
* run `composer start` or manually run `php -S localhost:8002 -t web/`
* open <http://localhost:8002> in browser

### Config Requirements:

* Copy `config/config.dist.php` to `config/config.php`
* Add github token
* Add repositories to get stats for

### Ignoring Certain Pull Requests

Sometimes a project has a PR open for review/discussion by the team and may inaccurately weigh down the repository stats by remaining open.  
This feature is (still thinking) to ignore certain PRs completely in the stats, or to display them but with a specific status ("wip") and/or  
with no impact on the weight of the repo. In essense, this PR is weightless

### Screenshot

![first screenshot](https://cloud.githubusercontent.com/assets/182954/4017368/576fd744-2a3f-11e4-9200-29745af1bf13.png)
