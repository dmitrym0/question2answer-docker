# question2answer-docker
Question2Answer docker image

## Using plain docker
TBA

## Using docker-compose
TBA


Here's an example of a `docker-compose.yml` file
```yaml
question2answer:
  image: disrvptor/question2answer
  ports:
    - "8080:80"
  links:
    - db:mysql
  environment:
    QUESTION2ANSWER_DB_USER: question2answer_user
    QUESTION2ANSWER_DB_PASSWORD: 123456
    QUESTION2ANSWER_DB_NAME: question2answer


db:
  image: mariadb
  environment:
    MYSQL_USER: question2answer_user
    MYSQL_PASSWORD: 123456
    MYSQL_DATABASE: question2answer
    MYSQL_ROOT_PASSWORD: <something secret>

```

# This Fork

* PHP 5.6 -> 7.2
* Q2A 1.7.3 -> 1.7.5
* Adds the following plugins
  * [NoahY/q2a-badges](https://github.com/NoahY/q2a-badges)
  * [jhubert/qa-hipchat-notifications](https://github.com/jhubert/qa-hipchat-notifications)
  * [zakkak/qa-ldap-login](https://github.com/zakkak/qa-ldap-login)
  * [arjunsuresh/q2a-xml-rpc](https://github.com/arjunsuresh/q2a-xml-rpc)
  * [nakov/q2a-plugin-open-questions](https://github.com/nakov/q2a-plugin-open-questions)
  * [q2a-projects/q2a-tag-descriptions](https://github.com/q2a-projects/q2a-tag-descriptions)
  * [arjunsuresh/categorydescription](https://github.com/arjunsuresh/categorydescription)
  * [arjunsuresh/tag-search](https://github.com/arjunsuresh/tag-search)
