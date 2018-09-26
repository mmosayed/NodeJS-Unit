# Building APIs: Express + Postgres

# Topics
- What is an API?
- RESTful APIs
- Designing APIs


# Lesson

## What is an API?

API stands for Application Programming Interface.

Now what does that actually mean? People throw around that term very casually, but don't actually understand the true concept of what an API is.

### The Problem

When you are building something (a product and/or service), there are often times many challenging problems to solve:

- How will my user communicate with my data?
- How will my client / other products communicate with my data?
- Should everyone have access to my data?
- Am I allowing others to interact with my data?

As you can see we keep talking about DATA. Infact data is very important to us, our users and the overall organization building the product. 

When building online applications, it's important to understand that you're something that uses the amassed data from various users. It's the applications job to manage that data and portray it accurately to all the different parties associated.

### The Solution

This is where APIs come in. APIs allow for a set of recipes to be called upon when necessary by the right parties. For example: 

- Your Mobile App may call an API to get all the weather information for the week.
- Your Dashboard may call an API to create new Cities to get weather for. 
- Your Website may call an API to get the forecast for a particular zip code. 
- Your Weather Balloon may call an API to send back atmospheric pressure, temperature, & humidity.
- You might sell your API to 3rd Parties to gain access to your weather data.

So as you can see, there is always a particular "party" sending a request to an API endpoint. Then there is a data "bank" where the appropriate data is gather and responded with.

## What is Restful API?

There are many ways an API can be created. It just matters on how much data needs to be passed and how frequently. For example, we can use different technologies to create APIs. We can use Sockets, TCP, HTTP. Restful APIs are built on top of HTTP.

REST is acronym for REpresentational State Transfer.

### Guiding Principles of REST
1. **Client / Server -** We differentiate the Client and Server. Server's job is to store and serve all data. Client's job is to portray and request that data. 
2. **Stateless -** Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
3. **Cacheable –** The ability to cache that data on the client side. The server lets the client know that the data can be cached.
4. **Uniform interface –** There's a pattern to how to retrieve data. There's a pattern on how the response is structured.
5. **Layered system –** Being able to divide up the APIs based on a specific feature or model. Also securing access to API based on the client accessing it.
6. **Code on demand –** Allows for the overall logic to change on the fly for any feature. Client can stay the same, but APIs can return newer data.

## Designing a RESTful API

### Instagram Clone

Let's work on a simple Instagram Clone! This clone should be able to do the following:

- Show a Newsfeed of all the latest posts
- Show a User's Profile and all their posts
- Click into a Post and see all the comments
- Leave a comment on a Post

### Identify Object Model

The very first step in designing a REST API based application is – identifying the objects which will be presented as resources.

