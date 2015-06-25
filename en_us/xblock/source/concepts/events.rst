.. _XBlocks, Events, and Grading:

#############################
XBlocks, Events, and Grading
#############################

Events are emitted by the server, the browser, or the mobile device to capture
information about interactions with the courseware.

In most cases, your XBlock must emit events. `Assigning a grade <Publish Grade
Events>`_ is a common event.

.. contents:: Section Contents:
 :local:
 :depth: 1
   
.. _Publish Events in Handler Methods:

**********************************
When an XBlock Should Emit Events
**********************************

Your XBlock should emit an event whenever a significant state change occurs,
and when a grade for the learner's interaction is assigned. For example, when a
learner submits an answer or otherwise interacts with your XBlock, an event
should record that action.

Your XBlock must emit an event to `assigning a grade <Publish Grade
Events>`_ to a learner.

Analysis of events can provide insight about how learners use the XBlock in the
runtime application. Using event data, analysts should be able to reconstruct
the state of the XBlock at any point in time.

**********************************
Publish Events in Handler Methods
**********************************

You define the events your XBlock emits in the XBlock's :ref:`handler methods
<Handler Methods>`.

In the handler method, you use the XBlock `runtime interface <Runtime Publish
Method>`_ ``publish`` method to emit the event. The ``runtime.publish`` method
causes the runtime application to save the event data in the application event
stream.

The following code shows the ``runtime.publish`` method syntax in an XBlock
handler:

.. code-block:: python

  self.runtime.publish(self, "event_type",
                       { event_dictionary })

Note the following information about the ``runtime.publish`` method.

* The ``event_type`` uniquely identifies the event in log files. 

* The event dictionary contains key-value pairs that define the event. 

********************
Publish Grade Events
********************

To assign a grade for a learner's interaction with the XBlock, the XBlock
handler method must publish a grade event.

A grade event is uses the ``runtime.publish`` method with specific arguments.

* The event type is ``grade``.

* The event dictionary must contain two entries.

  * ``value``: The learner's score
  * ``max_value``: The maximum possible score
  * ``user_id``: The ID of the user. Optional. If not specified, the current
    user's ID is used.

For example, the following handler code emits a grade for the learner that is
stored in the ``submission_result`` variable in an XBlock with the maximum
grade of ``1.0``.

.. code-block:: python

  self.runtime.publish(self, "grade",
                       { value: submission_result
                         max_value: 1.0 })

Typically, the handler method also returns the calculated grade, to be
displayed to the learner.

.. note:: 
 To be graded, in addition to publishing the grade event, the XBlock must also
 have a ``has_score`` variable set to ``True``.

.. include:: ../links.rst
