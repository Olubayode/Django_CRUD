# Django_CRUD


Created 20-06-2022 13:10:01

Author: Olubayode Ebenezer.

I Created a new GitHub repository with a README.md, and Python .gitignore file.

Cloned it to my machine/computer, that created a new folder on your computer with my repository’s content.

I Created a new virtual environment in that folder named env and installed django in it.

I Created a new django project. I use an ID as the name of the project.

I Created a new application using the django startapp command. The app should be called blog.

Add the blog app to the main_projects INSTALLED_APPS.

 

Replace the content of blog/models.py with the content of this src file:

https://github.com/Olubayode/Django_CRUD/blob/main/src/blog/models.py 

I now have a Post model in blog/models.py.

I Created migrations for my new model using the makemigrations django command. 

I Run all migrations using, migrate django command.

To make my Post model accessible from the admin site,  I registered the Post model in blog/admin.py 

 # Now for the views. 

In blog/views.py,  I created a new view/class PostListView, which inherits django’s generic ListView,  it’s config/attributes should be:

model = Post

 I Created another view, PostCreateView, which inherits django’s generic CreateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

I Created another view, PostDetailView, which inherits django’s generic DetailView, with attributes:

model = Post

 I Created another view PostUpdateView, which inherits django’s generic UpdateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 I Created another view PostDeleteView, which inherits django’s generic UpdateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

# Time to create templates.

I Created a new folder templates under the blog app.  

Copy all the files and folders from
 https://github.com/Olubayode/Django_CRUD/tree/main/src/templates to blog/templates folder.

 

I created a file, blog/urls.py, if it doesn’t already exist.

Replaced the content of blog/urls.py with the content of https://github.com/Olubayode/Django_CRUD/blob/main/src/blog/urls.py 

 
I went to my project_app/urls.py and add a new url pattern with the following content:

path("blog/", include("blog.urls", namespace="blog"))

 I Staged and Commit your Django project and push my changes to my GitHub repository. 

 
# Resources:


Django CRUD Functionality with CBVS CLASS BASED VIEWS  (https://www.youtube.com/watch?v=7sUEktXzxlA)

Working with the Terminal ( https://www.youtube.com/watch?v=lIVsa9tXdck&t=2297s)

Python Functions ( https://www.youtube.com/watch?v=V961_ncGTxg&t=11s)

Django CRUD (Create, Retrieve, Update, Delete) Function Based Views - GeeksforGeeks (https://www.geeksforgeeks.org/django-crud-create-retrieve-update-delete-function-based-views/)
