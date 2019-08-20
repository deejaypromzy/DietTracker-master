# DietTracker (in progress)
This repository holds the source code of DietTracker App, simple app which counts nutrients values of added food and compares it with chosen diet plan. 
The application is built as side project to increase programming experience and develop android skills.

Main features:
- set diet plan (daily calories limit, protein/carbs/fat percent ratio, meals)
- add food eaten (either a dish or a product)
- create dishes from products to make adding food easier
- browse through basic products data with 14 nutrients value from USDA Food Database @link https://ndb.nal.usda.gov/ndb/
- (in progress) nutrients value calculator
- (in progress) get full nutrient report about product from USDA Food Database
- (in progress) get daily, weekly, monthly statistics about nutrients eaten and diet plan success

Tools:
- Android Studio 2.3.3
- Android SDK Build Tools v25.0.2
- minSdkVersion 15

Technology used:
- Android Support Library v25.3.1 (all RecyclerViews, CardViews etc.)
- GSON serialization library (for saving objects in SharedPreferences)
- Android Data Binding (for binding layouts)
- SQLite Database with Content Provider

Project description:
Code of aplication is based on MVP pattern.

- Model - constists of database, shared preferences, files managers and classes which represents data used in application.
- View - either Activity or Fragment implementing corresponded View interface, which only responsibility is to get input from user
and display data prepared by model.
- Presenter - every View has its own presenter which is implementation of Presenter interface, which acts like a middle-man between
model and view. Presenter send to model received from view input and get the output from model to send to view.

Application is still under construction. Next goals to achieve:
- finish displaying added food in fragment containing food added in single day,
- add possibility to sort and filter product and dishes searching results,
- fix fragment management after configuration changes,
- add different layout support (phone landscape, tablet portrait and landscape)
- add nutrient calculator and full product report from USDA Food Database API,
- fix layouts to follow material design guidelines.
