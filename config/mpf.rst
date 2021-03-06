mpf:
====

*Config file section*

+----------------------------------------------------------------------------+---------+
| Valid in :doc:`machine config files </config/instructions/machine_config>` | **YES** |
+----------------------------------------------------------------------------+---------+
| Valid in :doc:`mode config files </config/instructions/mode_config>`       | **NO**  |
+----------------------------------------------------------------------------+---------+

.. overview

The ``mpf:`` section of your config is where you...

.. todo::
   Add description.

Optional settings
-----------------

The following sections are optional in the ``mpf:`` section of your config. (If you don't include them, the default will be used).

allow_invalid_config_sections:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (Yes/No or True/False). Default: ``false``

MPF will not raise a fatal error when on invalid section when you set this to true. This might be useful when you are developing a new feature and do not want to constantly update config_spec (the file which describes allowed sections).

auto_create_switch_events:
~~~~~~~~~~~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (Yes/No or True/False). Default: ``True``

MPF will post switch_event_active and switch_event_inactive (see below) when this is enabled.

default_flash_ms:
~~~~~~~~~~~~~~~~~
Single value, type: ``integer``. Default: ``50``

Default flash_ms for all flashers when not overwritten.

default_pulse_ms:
~~~~~~~~~~~~~~~~~
Single value, type: ``integer``. Default: ``10``

Default pulse_ms for all coils when not overwritten. This will be used when you do not specify any pulse_ms in your coil.

default_platform_hz:
~~~~~~~~~~~~~~~~~~~~

.. versionadded:: 0.33

Single value, type: ``number`` (will be converted to floating point). Default: ``1000.0``

For all platforms non-tickless platforms we poll this often.

save_machine_vars_to_disk:
~~~~~~~~~~~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (Yes/No or True/False). Default: ``true``

If set to true MPF will persist machine_vars to disk in a background writer.

switch_event_active:
~~~~~~~~~~~~~~~~~~~~
Single value, type: ``string``. Default: ``%_active``

If auto_create_switch_events is set to true this event will be posted after a switch turned active.

switch_event_inactive:
~~~~~~~~~~~~~~~~~~~~~~
Single value, type: ``string``. Default: ``%_inactive``

If auto_create_switch_events is set to true this event will be posted after a switch turned inactive.

switch_tag_event:
~~~~~~~~~~~~~~~~~
Single value, type: ``string``. Default: ``sw_%``

This event will be posted for all tags after a switch turned active.

default_show_sync_ms:
~~~~~~~~~~~~~~~~~~~~~

.. versionadded:: 0.32

Default sync_mc for all shows when not specified otherwise.
