# Swagger UI overview
https://idratherbewriting.com/learnapidoc/pubapis_swagger.html

https://swagger.io/resources/articles/documenting-apis-with-swagger/

Good user experience is key to using any product, and the same holds true for APIs. The better the interface that's used to conusme APIs, the higher the chance of achieving your business and technological objectives.

Since the advent of mobile and cloud computing, APIs have gone mainstream, with more and more companies and organiation understanding the business value of creating APIs. With a lot of web services emerging, the need to have clear API documentation for adopting these services became clear.

API documentation is the information taht is required to successfully consume and integrate with an API. This can be in the form of technical wrting, code samples and exampls for better understanding how to consume an API. Concise and clear documentation - which allows your API consumers to adopt it into their application quickly - is no longer optional for organizations that want to drive adoption of their APIS.

## Why documentaiton matters.
A servey by ProgrammableWeb found taht API consumers consider complete and accurate documentation as the biggest factor in their API decision making, even outweighting price and API perforamnce.

Good documentation accelerates development and consumpition, and reduces the money and time that would otherwise be spent answering suport calls. Documentation is part of the overall user experience, and is one of the biggest factors for increased API growth and usage.

## Challenges of API documentaion
APIs, like so many other products, tend to evolve rapidly during development and release cycles. Maintaining and updating this documentation for your development team and consumers, so they work with teh API efficiently, becomes a difficult process. This is especially true if you are using static documents, like a .pdf, to provide documentation to your end consumers. The second issue is facilitating interaction between multiple web services. Applications are made up of multiple services that constatnly communicate and interact with each other.

As Restful services grow in number, so do the programming languages that are used to implement them, making it harder for them to communicate. API documentation can be though of as the interface for consuming an API, and such, needs to facilitate interaction between these different web services. Regular API interfaces, be it text documentaion or others like Javadocs, do not allow them to communicate with each other. These challenges, along with other API pain points, led to the creation of the Swagger Specification.

In the next section, we will take a closer look at how the OpenAPI specification can help address your documentaiton challenges.

## Why use OpenAPI for API documentation
The swagger Specification, which was renamed to the OpenAPI specification (OAS), after the swagger team joined SmartBear and the specification was donated to the OpenAPI initiatie in 2015, has become the de factor standard for defining restful apis.

OAS defines an API's contract, allowing all the API's stakeholders, be it your development team, or your end consumers, to understand what the API does and interact with its various resources, without having to integrate it into their own application. This contract is language agnostic and human readable, allowing both machiens and humans to parse and understand what the API is supposed to do.

The OAS contract describes what the API does, it's request parameters and response objects, all without any indication of code implementaion. Web services defined with OAS can communicate with each other irrespective of the language they are built in, since OAS language3 agnostic and machine readable.

## How does OAS help with documentation?
One of the biggest reason why Swagger first gained adoption, was its ability to help streamline the documentation for RESTful APIs. using a tool like Swagger UI - either open source or within the SwaggerHub platform - you can convert your OAS contract into an interactive API console that consumers can use to interact with the API and quickly learn how the API is supposed to behave.

Generating documentation for your API is just one of the advantages of defining your API with OpenAPI. Other benefits includes:
* Help internal team members understand the API and agree on its attributes: An API definitioni allows documentatioin tools like the Swagger UI to visualize APIs. You can visualize all of our intenral APIS so that developers could use upstream and downstram services quickly and easily. Team-based tools like Swagger Hub allow collaboration on teh API's documentaion and host them for internal consumption.
* Hlep external folks understand the API and what it can do: Again, Swagger UI is a well-used visualization tool for documentaqion. Not just for intenral consumption, but for external adoption. The SwaggerUI has interactivity built in, so external consumers can try and every resource of an API and get comfortable with it before using it in their code base. Using the SwaggerHub platform, organizations can also provide controlled access to their external consumers.
* Create tests for your API: Your OAS definition provides a contract that describes what a successful response will look like when someone calls your API. This contract can also be re-purposed to generate test cases which can drastically descrease the amount of setup team needed for testing your APIs.
* Generate implementation code and SDKs: In addition to generating documentation, the OpenAPI definition can also be used to accelerate development by scaffolding implementaion code and SDKs for the APi. API defnitions files can be imported into a numbe rof different tools, like Swagger Codegen and SwaggerHub, to create these stubs code in many different languages.

Now that we've covered why your team should adopt OAS and Swagger tools into your API development workflow, the next question is how do you actually get started? In teh next section, we will take a closer look at different approaches to getting started with OAS.

## Aproach to OpenAPI
When it comes creating the OAS definition, two important schools of thoughts have emerged: The "Design First" and the "Code First" approach to API developement.

THe Design First approach advocates for designing the API's contract first before writing any code. This is a relatively new approach, but is fast catching on, especially with the use of OpenAPI. In the design-first approach, the API contract acts as the central draft that keeps all your team members aligned on what your API's objectives are, and how your API's resources are exposed.

Spotting issues in the design, before writing any code is much more efficient and streamlined apprach than doing so after the implementaion is already in place.

If your team is ready to transition to a design first approach, you will first need to get comfortable with writing an API definition. Here are some resources to help you get started in the process.

## "Code First" Approach
The code first approach is a more traditioanl approach to building APIs, with development of the code happening after teh business requirements are laid out, then the documentation of the API is done from the code.

For many API teams, getting started with OpenAPI means starting with a "code first" approach, and generating the definition from an existing set of APIs. let's explore a few of the other popular methods for generating an OAS definition when you already have existing APIs.

## Generating an OAS definition with Inspector
Swagger Inspector is an easy to use developer tool to quickly execute any API request, validate its responses and generate a corresponding OpenAPI definition. Use Swagger Inspector to quickly geneate your OAS-based documentaion for existing REST APIs by calling each end point and using the associated response to generate OAS compliant documentation, or string together a series of calls to generate a full OAS document for multiple API endpoints.

Perform quick API calls right from your browser window with Swagger Inspector. After you perform your first call, you can create a free account and save your call history within Inspector.

Swagger Inspector is integrated with SwaggerHub, the API design and documentation platform for teams. The integration allows developers to automatically host and visualize their API documentaiton on SaggerHub to enable API discovery and consumpiton by internal and external stakeholders.

## How to generate OpenAPI from exisitng APIs
Head over to Swagger Inspector, and insert the end point of the resource you want to have documented. You can navigate to teh right panel from the History section of Swagger Inspector, and click "create api definition" to create the OAS definition.

The cool thing about inspector is that you can select multiple end points and consolidate their documentation in one single OpenAPI file through a Collection.

After you create an account, you can easily access all your tests in your history, anywhere at any time, and also generate the corresponding OpenAPI specification with the clik of a button in inspector.

The generated definition will provide an OAS-compliant structure for your team to build out your API documentaiton. With the definition in place, you can add in important details like: supported content types, descriptions, examples, authentication types, and more.

# Buliding beautiful Rest APis using Flask, Swagger UI and Flask-RESTPlus
http://michal.karzynski.pl/blog/2016/06/19/building-beautiful-restful-apis-using-flask-swagger-ui-flask-restplus/

This article outlines steps needed to create a REST API using Flask and FLask-RESTPlus. These tools combine into a framework, which automates common tasks:
* API input validation
* formatting output (as JSON)
* generating interactive documentation (with Swagger UI)
* turning Python exceptions into machine-readable HTTP responses

## Flask
Flask is a web micro-framework written in Python. Since it is a micro-framework, Flask does very little by itself. In contrast to a framework like Django, which takes the batteries included approach, Flask does not come with an ORM, serializers, user management or built-in internationalization. All these features and many other others are available as Flsk extensions, which make up a rich, but loosely coupled system.

The chanllenge, then, for an asiring Flask developers lies in picking the right extensions and combining them together to get just teh right set of functions. In this article we will describe how to use the Flask-RESTPlus extension to create a Flask-based RESTful JSON API.

## Fkask-RESTPlus
Flask-RESTPlus aims to make building REST APIs quick and easy. It provides just enough syntacitc sugar to make your code readable and easy to maintain. Its killer feature is teh ability to automatically generate interactive documentation for your API using Swagger UI.

## Swagger UI
Swagger UI is part of a suite of technologies for docuenting RESTful web services. Swagger has enolved into the OpenAPI specification, currently curated by the Linux Foundation. Once you have an OpenAPI description of your web service, you can use software tools to generate documentation or even boilerplat code (client or server) in a variety of languages. Take a look at swagger.io for more information.

Swagger UI is a great tool for describing and visualizng RESTful web services. It generates a small webpage, which documents your API and allows you to make test queries using Javascript.

In this article we will describe how to use Flask and Flask-RESTPlus to create a RESTful API which comes equipped with Swagger UI.

## Geting started
To show off the features of Flsak-RESTPlus I repared a small demo application. It's a part of an API for blogging platform, which allows you to manage blog posts and categories.

## Prerequisites
You will need to have Python with Virtualenv and Git installed on your machine
I would recommend using Python 3, but Python 2 should work just fine.

## Setting up the demo appication
To download and start the demo application issue the following commands. First clone the applicaiton code into any directory in 

```
git clone https://github.com/postrational/rest_api_demo
cd rest_api_demo
```
Create a virtual Python environment in a directory named venv, activate the virtualenv and install required dependencies using pip:
```
virtualenv -p `which pyhton3` venv
source venv/bin/activate
pip install -r requirements.txt
```
Now let's set up teh app for development and start it:
```
python setup.py develop
python rest_api_demo/app.py
```
## Defining your Flask app and RESTPlus API
Flask and flask-restplus make it very easy to get started. Minimal code required to create a working API is just 10 lines long.
```
from flask import Flask
from flask_restplus import Resource, Api

app = Flask(__name__)   # Create a Flask WSGI application
api = Api(app)          # Create a Flask-RESTPlus API

@api.route('/hello')    # Create a URL route to this resource
class HelloWorld(Resource): # Create a Restful resource
    def get(self):
        return {'hello': 'world'}

if __name__ == '__main__':
    app.run(debug=True) # start a development server
```
To make the code more maintainable, in our demo dapplication we separate the app definition. API methods and other types of code into separate files.

The definition of the RESTPlus API is stored in teh file rest_api_demo/api/restplus.py, while the logic for configuring and starting the Flask app is stored in rest_api_demo/app.py.

The a look into the app.py file and the initialize_app function.
```
def initialize_app(flask_app):
    configure_app(flask_app)

    blueprint = Blueprint('api', __name__, url_prefix='/api')
    api.init_app(blueprint)
    app.add_namespace(blog_post_namespace)
    app.add_namespace(blog_categories_namespace)
    flask_app.register_blueprint(blueprint)

    db.init_app(flask_app)
```
This function does a number of things, but in particular it sets up a Flask blueprint, which will host the API under the /api URL prefix. The allows you to separate the API part of your applicaiton from other parts. Your app's frontend could be hosted in the same Flask application but under a different blueprint.

THe RESTPlus API itself is also split into a number of separate namespaces. Each namespace has its own URL prefix and is stored in a separate file in teh /api/blog/endpoints directory. In order to add these namespaces to the API, we need to use the api.add_namespace() functions.

initialize_app also sets configuration values laoded from settings.py and configures the app to use a database through the magic of Flask-SQLAlchemy.

## Defining API namespaces and restful resources
Your API will be organized using API namespaces, RESTful resources and HTTP methods. Namespaces, as described above, allow your API definitions to be split into multiple files, each defining a part of the API with a different URL prefix.

Restful resources are used to organize the API into endponts corresponding to different types of data used by your application. Each endpoint is called using a different HTTP method. Each method issues a different command to the API. For example, GET is used to fetch a resource from teh API, PUT is used to update its information, DELETE to delete it.
* GET /blog/categories/1 - Retrieve category with ID 1
* PUT /blog/categories/1 - Update the category with ID 1
* DELETE /blogcategories/1 - Delete the category with ID 1

Resources ususally have an associated collection endpoint, which can be used to create new resources (POST) or fetch lists(GET).

* GET /blog/categories - Retrieve a list of categories
* POST /blog/categories - Create a new Category

Using Flask-RESTPlus you can define an API for all of the endpoints listed above with teh following block of code. We start by creating a namespace, we create a collection, a resource and associated HTTP methods.

```
ns = api.namesapce('blog/categories', description='Operations related to blog categories')

@ns.route('/')
class CategoryCollection(Resource):
    def get(self):
        """Returns list of blog categories."""
        return get_all_categories()

    @api.response(201, 'Category successfully created.')
    def post(self):
        """Creates a new blog category."""
        create_category(request.json)
        return None, 201

@ns.route('/<int:id>')
@api.response(404, 'Category not found.')
class CategoryItem(Resource):
    def get(self, id):
        """Returns details of a capacity"""
        return get_category(id)

    @api.response(204, 'Category successfully updated.')
    def put(self, id):
        """Update a blog category."""
        udpate_category(id, request.json)
        return None, 204

    @api.response(204, 'Category successfully deleted.')
    def delete(self, id):
        """Deletes blog category"""
        delete_category(id)
        return None, 204
```



