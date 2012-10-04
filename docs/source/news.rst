Changelog
=========

0.14.6 / 2012-07-26
--------------------


- fix gevent & subproces
- fix request line length check
- fix keepalive = 0
- fix tornado worker

0.14.5 / 2012-06-24
--------------------

- fix logging during daemonisation

0.14.4 / 2012-06-24 
------------------- 

- new --graceful-timeout option
- fix multiple issues with request limit
- more fixes in django settings resolutions
- fix gevent.core import
- fix keepalive=0 in eventlet worker
- fix handle_error display with the unix worker
- fix tornado.wsgi.WSGIApplication calling error

- **breaking change**: take the control on graceful reload back.
  graceful can't be overrided anymore using the on_reload function.

0.14.3 / 2012-05-15 
-------------------

- improvement: performance of http.body.Body.readline()
- improvement: log HTTP errors in access log like Apache
- improvment: display traceback when the worker fails to boot
- improvement: makes gunicorn work with gevent 1.0
- examples: websocket example now supports hybi13
- fix: reopen log files after initialization
- fix: websockets support
- fix: django1.4 support
- fix: only load the paster application 1 time

0.14.2 / 2012-03-16 
-------------------

- add validate_class validator: allows to use a class or a method to
  initialize the app during in-code configuration
- add support for max_requests in tornado worker
- add support for disabling x_forwarded_for_header in tornado worker
- gevent_wsgi is now an alias of gevent_pywsgi
- Fix gevent_pywsgi worker

0.14.1 / 2012-03-02 
-------------------

- fixing source archive, reducing its size

0.14.0 / 2012-02-27  
-------------------

- check if Request line is too large: You can now pass the parameter
  ``--limit-request-line`` or set the ``limit_request_line`` in your
  configuration file to set the max size of the request line in bytes.
- limit the number of headers fields and their size. Add
  ``--limit-request-field`` and ``limit-request-field-size`` settings
- add ``p`` variable to the log access format to log pidfile
- add ``{HeaderName}o`` variable to the logo access format to log the
  response header HeaderName
- request header is now logged with the variable ``{HeaderName}i`` in the
  access log file
- improve error logging
- support logging.configFile
- support django 1.4 in both gunicorn_django & run_gunicorn command
- improve reload in django run_gunicorn command (should just work now)
- allows people to set the ``X-Forwarded-For`` header key and disable it by
  setting an empty string.
- fix support of Tornado
- many other fixes.

History
=======

.. toctree::
   :titlesonly:

   2011-news
   2010-news