 Installaltion :
Type
 step 1-->"git clone https:/pysantosh/djangocutter.git"
 on Cmd(windows) or Terminal(linux)
step 2 -->
"pip install -r development.txt" for running project
You may have occure error: NoReverseMatch at / 'djdt' is not a registered namespace

solutions: $ pip install django-debug-toolbar
  add this on config/urls.py
  """
from django.contrib import admin
from django.urls import path, include
from django.conf import settings

urlpatterns = [
    path('admin/', admin.site.urls),
]
if settings.DEBUG:
    import debug_toolbar
    urlpatterns += [path('__debug__/', include(debug_toolbar.urls))]


---->>>>For Changing the databse read "doc/environ.rst" <<<<----
