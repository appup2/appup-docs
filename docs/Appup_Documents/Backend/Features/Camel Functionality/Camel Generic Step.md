
**Camel Generic Step:**

**Objective:**

It is a versatile open-source integration framework based on known
Enterprise Integration Patterns. **Camel** empowers you to define
routing and mediation rules in a variety of domain-specific languages.

**Attributes:**

  **Attributes**        **Description**
  --------------------- -----------------------------------------------------
  **URI**               To Enter Endpoint URI
  **Body**              To Enter message body to producer
  **Value Type**        To select type as free marker template or handlebar
  **Headers**           To Enter headers to uri
  **Output Variable**   To Enter header key of response from end route

**Sample config.json:**

{

**"workflows"**: \[

{

**"id"**: 22542,

**"name"**: **"camel"**,

**"trigger"**: **"rest"**,

**"expression"**: **"camel"**,

**"method"**: **"GET"**,

**"steps"**: \[

{

**"uri"**:**"aws-s3://appup-bucket?region=US\_EAST\_1&accessKey=AKIAIVJMBGBK4PRJ3SKA&secretKey=RAW(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)"**,

**"value\_type"**: **"hb"**,

**"body"**: **"Hello world"**,

**"output\_variable"**: **"output"**,

**"type"**:**"camel-custom-step"**,

**"headers"**:**"CamelAwsS3Key=test/ghhjj.txt ,
CamelAwsS3BucketName=appup-bucket"**,

**"id"**: **"1"**,

**"next"**: {

**"success"**: **"3"**,

**"failure"**: **"hangup"**

}

},

{

**"variable\_name"**: **"output"**,

**"http\_response\_code"**: **"200"**,

**"response\_content\_type"**: **"text/html"**,

**"value\_type"**: **"hb"**,

**"type"**: **"send"**,

**"id"**: **"3"**,

**"next"**: {

**"success"**: **"hangup"**,

**"failure"**: **"hangup"**

}

}

\]

}

\],

**"filters"**: \[\],

**"server"**: {},

**"plugins"**: \[

\]

}



**Executor Description:**

In executor class first create a json object to perform action and send
body data to producer and as a response from end route will receive from
consumer based on the end route which we provided the step uri .If any
exception occur then set status to failure.
