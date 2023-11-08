
## Automated Testing

A lot of work went into making some automated tests for the server side.
However, the testing approach is fairly non-standard for now.
The tests are not all the way end-to-end.  They run all the way from the 
service to the database.
So, we really just skipped where the controllers call the services - which
is pretty trivial stuff anyway.

### Environment

You need to set up as you would for any other server. That process is 
described elsewhere. Briefly,
1. you need a database, and it needs to be empty to begin with.
2. you have to create a server config file for your test server.  I have no 
imagination, so I usually call it test.env.
3. you need edit that file with things like database config, **but you need to 
   take particular care** to set this configuration knob in the file.
```dotenv
NODE_ENV=test
```
After that, I usually run the tests from within WebStorm.  
When you run your tests, the server finds you config file using the FACILITY 
env variable:
```bash
export FACILITY=test
```

### Approach to Testing

All the complicated logic lies in the servers and repos, so I test there and 
test thoroughly.  I do not worry about controllers.
I just do not understand everyone saying "unit test, unit test" - I'm way 
too lazy to mock every little thing.  Plus, the compile and test cycle is so 
fast, that there is really no reason to run stuff right to the database.

I number tests with big random(ish) numbers. Rationale is given below.

I also like to run against an empty database. Every test that sticks objects in 
the database is responsible for taking them out again.  Also, every test that 
sticks objects in the database sticks the test number in the comment field 
of the object.  That way it's easy to figure out what test left what crap 
lying around the database (by accident).

I tend to use random numbers (converted to strings) for fields that have to 
be unique (like names or nicknames).  This reduces the chances of tests run in 
parallel to fight with 
each other. Even more so it takes all the burden of the test writers to keep 
coming up with uniques stings for things like mutation names.

### Running Tests

TBD. Just using Webstorm tools.

### Debugging

The webstorm tools are great.  They point you at the test case and the code 
when things go wrong.

Note that the policy of sticking the test number in any object that goes 
into the database makes it super easy to track down the source of stray 
objects if test cases fail to clean up after themselves.



