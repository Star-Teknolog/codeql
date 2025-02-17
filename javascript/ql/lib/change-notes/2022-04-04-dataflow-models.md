---
category: breaking
---
* Many library models have been rewritten to use dataflow nodes instead of the AST.
  The types of some classes have been changed, and these changes may break existing code.
  Other classes and predicates have been renamed, in these cases the old name is still available as a deprecated feature.

* The basetype of the following list of classes has changed from an expression to a dataflow node, and thus code using these classes might break. 
  The fix to these breakages is usually to use `asExpr()` to get an expression from a dataflow node, or to use `.flow()` to get a dataflow node from an expression.  
   - DOM.qll#WebStorageWrite
   - CryptoLibraries.qll#CryptographicOperation
   - Express.qll#Express::RequestBodyAccess
   - HTTP.qll#HTTP::ResponseBody
   - HTTP.qll#HTTP::CookieDefinition
   - HTTP.qll#HTTP::ServerDefinition
   - HTTP.qll#HTTP::RouteSetup
   - NoSQL.qll#NoSql::Query
   - SQL.qll#SQL::SqlString
   - SQL.qll#SQL::SqlSanitizer
   - HTTP.qll#ResponseBody
   - HTTP.qll#CookieDefinition
   - HTTP.qll#ServerDefinition
   - HTTP.qll#RouteSetup
   - HTTP.qll#HTTP::RedirectInvocation
   - HTTP.qll#RedirectInvocation
   - Express.qll#Express::RouterDefinition
   - AngularJSCore.qll#LinkFunction
   - Connect.qll#Connect::StandardRouteHandler
   - CryptoLibraries.qll#CryptographicKeyCredentialsExpr
   - AWS.qll#AWS::Credentials
   - Azure.qll#Azure::Credentials
   - Connect.qll#Connect::Credentials
   - DigitalOcean.qll#DigitalOcean::Credentials
   - Express.qll#Express::Credentials
   - NodeJSLib.qll#NodeJSLib::Credentials
   - PkgCloud.qll#PkgCloud::Credentials
   - Request.qll#Request::Credentials
   - ServiceDefinitions.qll#InjectableFunctionServiceRequest
   - SensitiveActions.qll#SensitiveVariableAccess
   - SensitiveActions.qll#CleartextPasswordExpr
   - Connect.qll#Connect::ServerDefinition
   - Restify.qll#Restify::ServerDefinition
   - Connect.qll#Connect::RouteSetup
   - Express.qll#Express::RouteSetup
   - Fastify.qll#Fastify::RouteSetup
   - Hapi.qll#Hapi::RouteSetup
   - Koa.qll#Koa::RouteSetup
   - Restify.qll#Restify::RouteSetup
   - NodeJSLib.qll#NodeJSLib::RouteSetup
   - Express.qll#Express::StandardRouteHandler
   - Express.qll#Express::SetCookie
   - Hapi.qll#Hapi::RouteHandler
   - HTTP.qll#HTTP::Servers::StandardHeaderDefinition
   - HTTP.qll#Servers::StandardHeaderDefinition
   - Hapi.qll#Hapi::ServerDefinition
   - Koa.qll#Koa::AppDefinition
   - SensitiveActions.qll#SensitiveCall