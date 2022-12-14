



<!-- ABOUT THE PROJECT -->
## About The Project:

![Home Page][product-screenshot1]
![Teams Page][product-screenshot2]
![Games Page][product-screenshot3]
![Hierarchy][product-screenshot4]

## The Goal:
The goal of this project was to build a full Front-End application using React.js using what i learned as a GA student.  Using this app you can a NBA team's Roster and Upcoming Games. You can also see games from the 2021 season.





### Built With:


* [![React][React.js]][React-url]
* [![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)](https://www.javascript.com/)
* [![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)](https://html.com/)
* [![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)]()




<!-- GETTING STARTED -->
## Launching:


<h3>Supported Platforms-</h3>
<em>Because of the use of WebKit Css, some plateform are not fully supported</em>

![macOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white)
![Safari](https://img.shields.io/badge/Safari-000000?style=for-the-badge&logo=Safari&logoColor=white)





<h1>Link to deployed site:<h1>
[[@NBA Stats](https://nba-stats-theta.vercel.app)]


## Components:
| Components 	| Description                                                                             	|
|------------	|-----------------------------------------------------------------------------------------	|
| App        	| My main component where all my componnets connect(parent)                               	|
| Home       	| Home component is the first component you see when loading up the website               	|
| Nav        	| This component host my nav with links to all other pages                                	|
| Teams      	| This component lists out all the teams                                                  	|
| TeamsInfo  	| This component displays minor information of the selected team from 'Teams'             	|
| Roster     	| This component displays every player of the selected team from 'Teams'                  	|
| Games      	| This component displays today's games with the option of viewing upcoming or past games 	|

## Time Freams:
| Component 	| Priority 	| Time Invested 	| Time Styling 	|
|-----------	|----------	|---------------	|--------------	|
| Teams     	|     H    	|       4h      	|      3h      	|
| TeamsInfo 	|     H    	|       2h      	|      2h      	|
| Nav       	|     M    	|      30m      	|      30m     	|
| Roster    	|     H    	|       3h      	|      3h      	|
| Games     	|     H    	|       6h      	|      2h      	|
| Home      	|     M    	|       2h      	|      1h      	|



<!-- ROADMAP -->
## Roadmap-

- [ ] More information for each team (e.g. wins/losses, record for current season, all time stats)
- [ ] Search feature to be able to search by player or team
- [ ] A more detailed roster page with players puctures and stats
- [ ] Sign in feature so you can favorite teams




## Current Issues
<h2> Issue #1<h2>
Currently the date is one day aheadthe Api was made in another time zone/region, i made a function to change the time. i had the same issue with the time but i fixed it.

```js
//data from api ex. -> 
{start: '2022-11-18T03:00:00.000Z'}

//how i got the correct time ->
   let time = game.date.start
   let givinTime = time.substring(12, 16)
   let timeSplit = givinTime.split('')
   let i = parseInt(timeSplit[0]);
   i = i + 7
   timeSplit[0] = i.toString()
   let newTime = timeSplit.join('')
   return(newTime)

// output = 10:00

```
I just need to do the same with the date but since the api searched using the date i will need it to display the correct date but search using the api's date

- [x] Resolved?

<h2> Issue #2<h2>
Pages does not display correctly on some screen sizes

- [ ] Resolved?

<h2> Issue #3</h2>
Day 1 of the project i was working on my home screen and i added a video as my home background, this video exceeded Github's file size limit which rendered my files unable to push. Not thinking anything off i continued throughout the project planning to just swap out the video with a link to the video, not knowing my old commits still included the video and would this need to push it.

Fix(provided by [[@davidmagbee](https://www.github.com/davidmagbee)])-

I first duplicated my files just in case i break/lose the original.
Then i ran this code directly in the directory of the original project while targeting the src folder for the video

```
git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch ./src/assets/nbamix-1080p.mp4" HEAD

```

- [x] Resolved?


<h2> Issue #4</h2>

My Page was trying to render information before it could get that information from the API so the page would break

Fix(provided by [[@jhorak])-

a conditional rendering statement- if my state whe the information is empty(falsy || < 0), render h1 tags with 'Loading' in it and set my loading state to true which would cause my useEffect to keep checking to see if the api brought back the Info. if the state be full(truthy || > 0), display the information on the screen.

(example code, actual code can be found in TeamsInfo.js)
```js
if (matchingTeam.length > 0) {
        return (
            <div className="teams-info-container">
                <h1 className="teams-info-name">{matchingTeam[0].name}</h1>
                <h1 className="team-code">{code}</h1>
            </div>
        )
         }else {
            return(
               setLoading(true)
               <div className="teams-info-container">
                <h1 className="teams-info-name">Loading</h1>
                <h1 className="team-code">Loading</h1>
            </div>
            )
         }
                   
            
```
- [x] Resolved?






<!-- CONTACT -->
## Links

[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jahimecameau/)







<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot1]: https://i.imgur.com/I34YAFC.png
[product-screenshot2]: https://i.imgur.com/jveZWp8.png
[product-screenshot3]: https://i.imgur.com/28Lcwpl.png
[product-screenshot4]: https://media.git.generalassemb.ly/user/43717/files/498aac89-84a7-4793-b86d-eae5376e056e
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
