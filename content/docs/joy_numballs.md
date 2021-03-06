Syntax
------

**INT** joy\_numballs ( \[ &lt;**INT** JoyID&gt; \] )

Description
-----------

Returns the number of [balls](joystick#ball "wikilink") on the specified
[joystick](joystick "wikilink"). If no joystick is specified, the number
of balls on the currently [selected
joystick](selected_joystick "wikilink") will be returned.

The JoyID is optional, if it is not present, the function uses the
selected joystick. You can change the selected joystick with
joy\_select().

Parameters
----------

  ------------------- -------------------------------------------------------------------------
  \[**INT** JoyID\]   - The [JoyID](JoyID "wikilink") of the [joystick](joystick "wikilink").
  ------------------- -------------------------------------------------------------------------

Returns
-------

**INT** : The number of [balls](joystick#Ball "wikilink").

<Category:functions> <Category:Joystick> <Category:Mod_joy>
