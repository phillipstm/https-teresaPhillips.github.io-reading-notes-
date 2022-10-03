# Event Driven Applications

## Event Driven Applications

<https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming>

**What native Node.js module allows us to get started with Event Driven Programming?**

EventEmitter

We access the EventEmitter class through the events module.

const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;

**What is the value of Object Oriented Programming used in tandem with Event Driven Programming?**

The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.

**Consider your knowledge of Event Driven Programming in the Web Browser, now explain to a non-technical friend how Event Driven Programming might be useful on the backend using Node.js.**

Event Driven Programming is a logical pattern that is used to confine code to small blocks that serve only one purpose to avoid issues of complexity and collision. It uses two concepts and Event Handler and a Main Loop listener. Like the web, when visiting a website each time you click something on a page an event is triggered, and each event has an associated function.

## Bookmark and Review

## Node docs: events ALL THINGS EVENT EMMITER

<https://nodejs.org/api/events.html>

## Things I want to know more about

import { EventEmitter } from 'node:events';
