# The JSONTree Spec

JSON is the de-facto data format for communicating. First appeared in web applications, the use of JSON has dramatically increased in recent years. The increasing research interest in IoT and embed systems, resulted in a wider adoption of JSON documents. [Code generators](https://quicktype.io/) and [server implementations](https://github.com/anttiviljami/openapi-backend) rely on JSON schemas to feed them with required data. There are also many tools like [documentation generators](https://github.com/Rebilly/ReDoc), [specification validators](https://github.com/p1c2u/openapi-spec-validator), [IDEs](https://github.com/swagger-api/swagger-editor) and others that have to analyze, parse, validate, and even transform, files written as JSON documents. Those requirements changed the way we handle these kind of documents. We cannot rely strictly in parsing mechanisms anymore, but need a way to store metadata such as location and range information.

There are many other use cases that we have not imagined yet. We expect that tools which parse, analyze and manipulate JSON documents will rise in the next years, increasing the need for a formal way to operate on JSON documents. This specification is intended to act as a community standard for people involving in building and maintaining such tools. 

The complete specification can be found in `jsontree.md`. Examples are provided under `examples` folder.

## Discussion

We are on the road to finalize the JSONTree and start spreading the idea to wider audiences. This repository will serve as the main point of reference for JSONTree standard, where people can propose, reject and evolve the specification to meet the community needs. 

You are very welcome to participate in our effort. If you have any suggestion, objection or any other general question, file a new issue.

## Participating Members

- George Gkasdrogkas ([@georgegkas](https://github.com/georgegkas))

