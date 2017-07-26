###Simple web request benchmark

Originally published: 2005-10-17 18:55:51
Last updated: 2006-10-31 00:27:13
Author: Josiah Carlson

Recently, there has been a discussion between myself and another individual as to the performance of particular web servers under certain situations.  Being that web server testing frameworks have different ways of measuring how long a 'request' takes, I thought I would take the guesswork out of it and measure everything explicitly.\n\nThere are generally 5 portions to a web request:\n1. create the connection\n2. start sending the request\n3. finish sending the request\n4. start recieving the response\n5. finish reading the response\n\nThis recipe measures the amount of time to perform each portion of a request to a single file many times, and prints the results in a somewhat reasonable fashion.