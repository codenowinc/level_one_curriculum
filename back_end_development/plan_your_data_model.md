# Plan Your Data Model
The typical first step when creating a database is to create a data model, which is a representation of the real world items in your application. For the example application we have todos. A todo is something that exists in the real world, and a data model of a todo would be the database representation of that real world item.

In our case, we are all building a simple todo list application which has todos. Thus we'll begin with the data model for todos.

## Mapping Out the Todo Model
We'll start by identifying all the pieces of information associated with a todo. All todos have a unique identifier called id (of type integer), a description (of type string), a pomodoro_estimate (of type integer), and a complete status (of type boolean).

>Briefly review the concept of datatypes with your students. Explain how ids are automatically included in the models as a unique identifier for every row of information stored in the database.

If we had to visualize our data model for a todo, it would look something like this.

![Todo Data Model](/images/plan_your_data_models/01.png "Todo Data Model")

But before we can create our database in our Rails applications, there is some house keeping we have to do.
