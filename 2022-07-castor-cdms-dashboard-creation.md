# CDMS Dashboard Creation

## When

February 2022 - July 2022

## Context

Castor CDMS was lacking the ability to show data to users to provide them insights on their current study status, for this reason the project has been bootstrapped to solve this issue. 
This project needed to be delivered as soon as possible so pressure was applied by executives.

## Goal

Create a dashboard with various representation of data stored within the application so that users have a clear understanding on how things are going on and take action accordingly.

## People

I worked with Nicolas Barrera who owned the whole FE part of the application and Nienke Tjalma as PO. Also, other people were involved in the project.

## How

I have been the only backend software engineer working at this so I had to deal with several parts of the business domain in order to understand how to properly extract data taking into account all the constraints.

The first iteration was focused on providing data without deeping too much into performance. Still, the final design was quite elegant, I used a Request-Generator-Response approach using a factory to retrieve the correct generator based on the request object.

The request object was decorated along the way by some decorators in order to centralize several necessities such as: limit visibility to objects not visible to the user, providing a cached version of a response.