---
layout: post
title:  "Building a Movie Explorer With React"
date:   2018-02-05 10:30:00 -0800
categories: portfolio
---

I recently wanted to see what it was like to use react for a front end application using some open api for data. I decided to make a movie exploration tool. 

## Choosing the right tools
I needed to choose the tools around react that I would use to build the project. I felt that it was important to use ES6 rather than older javascript. I enjoy keeping up with what's coming next in front end development. I also learned about webpack which would be great for enhancing download speed and size. I looked at various scaffolding solutions that incorporated these tools. I settled on `create-react-app` because it seemed robust, supported by official react entities, and popular. Into that I mixed a bootstrap based react component library called `react-bootstrap` which made it easy to lay things out.

### What not to use
I didn't want to add unnessesary tools that would be overkill for what I was doing. Redux is a popular tool to pair with react, but because I was keeping things fairly simple I didn't use it.

## Designing
I broke the interface into components: one master component that rendered navigation and the appropriate view (favorites or search). The sub views were broken into smaller functional components: 

```
App
└── Search View
│   └── <Navigation/>
│   └── <MovieDetail/>
│   └── <SearchPanel/>
│       └── <SearchForm/>
│       └── <SearchResults/>
│           └──[<MovieSmallCard/>]
│
└── Favorites View
    └── <Navigation/>
    └── <Faves/>
        └── [<Movie/>]
```

## Passing data around
This project gave me a grasp of react's data and function binding. Without having some globally available data object, components must propagate any relevant data and function calls back up the tree.

## Conclusion
React and ES6 are both great, I can now see why react has quickly gained popularity.

The project resides here:
[https://github.com/evfrenkel/omdb-movie-manager][proj]

[proj]: https://github.com/evfrenkel/omdb-movie-manager