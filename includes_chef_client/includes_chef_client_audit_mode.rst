.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The |chef client| may be run in |chef client_audit|. Use |chef client_audit| to evaluate custom rules---also referred to as audits---that are defined in recipes. |chef client_audit| may be run in the following ways:

* By itself (i.e. a |chef client| run that does not build the resource collection or converge the node)
* As part of the |chef client| run, where |chef client_audit| runs after all resources have been converged on the node

Each audit is authored within a recipe using the ``control_group`` and ``control`` methods that are part of the |dsl recipe|. Recipes that contain audits are added to the run-list, after which they can be processed by the |chef client|. Finished audits are first reported back to the |chef server|, and then to the |chef analytics| platform for further analysis, such as rules processing (for notification events triggered by expected or unexpected audit outcomes) and visibility from the actions web user interface.

