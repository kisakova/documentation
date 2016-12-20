.. _user-guide-activities-comments:

Add Comment
===========

.. warning:: Reused from OroCRM. Rework.

Interaction between users is an important part of successful work. In order to enable users to leave comments on records
of an :term:`entity <Entity>` or on details of an :ref:`activity <user-guide-activities>`, other than a contact request 
(e.g. leave some additional details of task, comment on an email sent or a call made, etc.) use the "*Add Comment"* 
action.

.. note::

    Comments are available for any activity or entity that has the Comments activity 
    :ref:`enabled <user-guide-activities-enable>`.


Create and View Comments
------------------------

You can make a comment when viewing or editing the item deatils, and also at the linked activity details. 

.. caution::

   The ability to view and write comments depends on the permissions and role settings defined in the system for the 
   Comment entity.


On these pages, the user should: 

- Click the :guilabel:`Add Comment` button.

- Enter the comment into the the text-box.

- Click the :guilabel:`Choose File` button to add a file to the comments.

- Click the :guilabel:`Add Comment` button to save the comment.

.. hint::

    You can :ref:`edit <user-guide-entity-management-edit>` the *Comment* entity and add new fields, if required.

For example, Ellen Rowel was a task "Email change needed", which required her to change the email address of 
Mr. Jeffrey Maynard.

- First, Ellen Rowel opened the "My Tasks" grid.

.. image:: /completeReference/img/common/activities/comments_01.png  

- Then she went to the View page of the task and left a comment.

.. image:: /completeReference/img/common/activities/comments_02.png  

- John Doe opened the task details on the View page of Jeffrey Maynard's contact record.

.. image:: /completeReference/img/common/activities/comments_03.png 

- Then he left a comment and attached Maynard's profile to it.
  
.. image:: /completeReference/img/common/activities/comments_04.png 

- Michael Buckley from the Marketing department opened the Tasks grid and opened the task View page. He can see both 
  comments made by Ellen Rowel and John Doe.

  .. image:: /completeReference/img/common/activities/comments_05.png 

   
Case Comments
-------------

Case comments work in a similar manner, except there is an additional check-box - "Make Public". You can use it to 
define if the comment shall be public on :ref:`Zendesk <user-guide-zendesk-integration>`. 

  .. image:: /completeReference/img/common/activities/comments_case.png 
