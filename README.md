play-embedded-mongo
===================

Trait to run functional tests in Play2 against embedded MongoDB

Use like so:

```
class IntegrationSpec extends PlaySpecification with EmbeddedMongo {

  "test some services" in new WithServer(new FakeApplication(additionalConfiguration = inMemoryMongoDatabase())) {
  	//hit the database here

  }
}
'''
