Access Purdue Course Catalog API

Drupal 7 module that pulls data from Purdue course catalog API xml feeds.

Provides blocks for:
 • plan of study
 • list of courses for college, department, or program
 • course data

External requirements (admin page):
 • Application key from registrar
 • Catalog ID number


Data structure requirements:

For courses:
 • /courses node exists
 • /courses/course node exists
 
For plan of study and required major courses:
degree content type with program ID field "field_course_catalog_id"
 • degree "required major courses" block shown on degree page
 • degree "plan of study" node is a child of a degree page with program ID.
 • degree "courses" node is a child of the degree node.

Next steps: 
Summer 2017: Because of the complex and inconsistent data structure created by the registrar while imputing data, this will be converted to a extension/submodule of the XML Feeds module.

Contact for implementation assistance:
Matt Bosma
mbosma@purdue.edu
