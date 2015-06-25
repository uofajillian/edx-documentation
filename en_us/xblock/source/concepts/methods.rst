.. _XBlock Methods:

####################
XBlock Methods
####################

You use XBlock methods in the XBlock Python file to define the behavior of your
XBlock.

.. contents:: Section Contents:
 :local:
 :depth: 1
   
.. _View Methods:

***************
View Methods
***************

XBlock view methods are Python methods invoked by the XBlock runtime to render
the XBlock.

An XBlock can have multiple view methods. For example, an XBlock might have a
student view for rendering the XBlock for learners, and an editing view for
rendering the XBlock to course staff. The XBlock view name to use is specified
in the runtime.

See :ref:`edX LMS <EdX Learning Management System as an XBlock Runtime>`
and :ref:`edX Studio <EdX Studio as an XBlock Runtime>` for information about the view requirements in these edX Platform XBlock runtime applications.

Typically, you define a view to produce a fragment that is used to render the
XBlock as part of a web page. Fragments are aggregated hierarchically. You can
use the user state, settings, and preferences to affect the rendering of the
XBlock as needed. 

In the following example, the Thumbs sample XBlock in the XBlock SDK defines a
student view.

.. include:: ../reusable/code_thumbs_student_view.rst

Although view methods typically produce HTML-based renderings, they can be used
for other purposes. You must ensure that the runtime description of each view
is clear about what return type is expected and how it will be used.

.. _Handler Methods:

***************
Handler Methods
***************

XBlock handler methods are Python methods invoked by AJAX calls from the user's
browser. Handler methods accept an HTTP request and return an HTTP response.

An XBlock can have any number of handler methods. For example, a problem XBlock
might contain ``submit`` and ``show_answer`` handler methods.

Each handler method has a specific name that is mapped to from specific URLs by
the runtime. The runtime provides a mapping from handler names to specific URLs
so that the XBlock JavaScript code can make requests to its handlers. Handlers
can be used with ``GET`` and ``POST`` requests.

Handler methods also emit events for learner interactions and grades. For more
information, see :ref:`Publish Events in Handler Methods`.

In the following example, the Thumbs sample XBlock in the XBlock SDK defines a
handler for voting.

.. code-block:: python

    def vote(self, data, suffix=''):  # pylint: disable=unused-argument
        """
        Update the vote count in response to a user action.
        """
        # Here is where we would prevent a student from voting twice, but then
        # we couldn't click more than once in the demo!
        #
        #     if self.voted:
        #         log.error("cheater!")
        #         return

        if data['voteType'] not in ('up', 'down'):
            log.error('error!')
            return

        if data['voteType'] == 'up':
            self.upvotes += 1
        else:
            self.downvotes += 1

        self.voted = True

        return {'up': self.upvotes, 'down': self.downvotes}

.. include:: ../links.rst