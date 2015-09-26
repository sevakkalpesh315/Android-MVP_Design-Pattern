# Android-MVP_Design-Pattern
Model-View-Presenter (MVP) is a variation of the Model-View-Controller (MVC) pattern but specifically geared towards a page event model.

MVP Pattern
Model-View-Presenter (MVP) is a variation of the Model-View-Controller (MVC) pattern but specifically geared towards a page event model. 
The primary differentiator of MVP is that the Presenter implements an Observer design of MVC but the basic ideas of MVC remain the same: the model stores the data, the view shows a representation of the model, and the presenter coordinates communications between the layers. 

Explanation of Modules
Model:
The model in MVP is just the same, that is described earlier in the Model-View-Controller pattern.
Presenter:
The Presenter’s responsibility is to handle user input and use this to manipulate the model data. The interactions of the User are first received by the view and then passed to the presenter for interpretation. Often, a presenter will maintain a selection that identifies a range of data in the model that is current, and the gestures received from the view will be used to act on this. There is One-to-One relationship between View and Presenter, means each view will be handled by one presenter.
View:
When the model is updated, the view also has to be updated to reflect the changes. View updates can be handled in several ways.

Passive view and Supervising Controller
The Model-View-Presenter variants, Passive View and Supervising Controller, specify different approaches to implementing view updates. 
In Passive View, the presenter updates the view to reflect changes in the model. The interaction with the model is handled exclusively by the presenter. The view is not aware of changes in the model.
In Supervising Controller, the view interacts directly with the model to perform simple data-binding that can be defined declaratively, without presenter intervention. The presenter updates the model; it manipulates the state of the view only in cases where complex UI logic that cannot be specified declaratively is required. .NET Data-binding technologies make this approach more appealing for many cases, although if not carefully designed it may result in coupling between view and model.

Advantages of MVP
As with Model-View-Controller, Model-View-Presenter has the advantage that it clarifies the structure of our user interface code and can make it easier to maintain.
Not only do we have our data taken out of the View and put into the Model, but also almost all complex screen logic will now reside in the Presenter.
We have almost no code in our View apart from screen drawing code Model-View-Presenter also makes it theoretically much easier to replace user interface components, whole screens, or even the whole user interface (Windows Forms to WPF for example). 
This makes the user opinion sensitive UI part perfectly separate of other parts of the application, hence it’s features can be enhanced separately with more involvement from the customer.
In addition unit testing the user interface becomes much easier as we can test the logic by just testing the Presenter. 

Disadvantages of MVP
Requires high skilled experienced professionals who can identify the requirements in depth at the front before actual design.
It requires the significant amount of time to analyze and design.
This design approach is not suitable for smaller applications. It overkills the small applications.
It can be hard to debug events being fired in active Model-View-Presenter.
The Passive View version of Model-View-Presenter can lead to a certain amount of boilerplate code having to be written to get the interface into the View to work.
In both MVP and MVC cases the code for supporting the proper pattern implementation can be complex, hence it is not advised to use in smaller projects.
