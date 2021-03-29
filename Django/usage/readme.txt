** Example use of dynamic urls:
path('members/<name>', views.members, name='members'),

** Example for using dynamic url in html with a parameter
href="{% url 'main_app:members' member.name %}" redirects to <mentioned url>/<member.name>