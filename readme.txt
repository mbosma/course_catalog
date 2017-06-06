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

For all college courses:
 • /courses node exists
 • /courses/course node exists
 • block "All College Courses" assigned to "courses" page
 • block "Course Data" assigned to "courses/course" page
 • add a field "Course Catalog Name", type = "Text" to a content type. Preferably a unique department content type.   The machine name of the field needs to be "field_course_catalog_name"
 • Edit all of the department nodes and add the department name to the field. 
   Example: "School of Aviation and Transportation Technology"
 
 For a list of all department courses on a subpage "courses" of a degree page:
 • degree content type with program ID field "Course Catalog ID". Machine name "field_course_catalog_id"
 • add a "courses" node as a child node of the degree node. Requires "Node Hierarchy" module
 • block "Degree subpage - List of Courses" block assigned to the new courses page
 
For plan of study and required major courses:
 • degree content type with program ID field "Course Catalog ID". Machine name "field_course_catalog_id"
 • degree "required major courses" block shown on degree page
 • degree "plan of study" node is a child of a degree page with program ID.
 • degree "courses" node is a child of the degree node.

Next steps: 
Summer 2017: Because of the complex and inconsistent data structure created by the registrar while imputing data, this will be converted to a extension/submodule of the XML Feeds module.

Contact for implementation assistance:
Matt Bosma
mbosma@purdue.edu
