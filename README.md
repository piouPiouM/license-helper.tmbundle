License Helper TextMate Bundle
==============================

Installation
------------

### To install with Git:

    cd ~/Library/Application\ Support/TextMate/Bundles
    git clone git://github.com/piouPiouM/license-helper.tmbundle.git "License Helper.tmbundle"
    osascript -e 'tell app "TextMate" to reload bundles'

### To install without Git:

    cd ~/Library/Application\ Support/TextMate/Bundles
    wget http://github.com/piouPiouM/license-helper.tmbundle/tarball/master
    tar zxf license-helper.tmbundle*.tar.gz
    rm license-helper.tmbundle*.tar.gz
    mv license-helper.tmbundle* "License Helper.tmbundle"
    osascript -e 'tell app "TextMate" to reload bundles'

Usage
-----

Use the tab trigger `license` and select a license to insert.

A license block is inserted as a Snippet. Use the tab key to move the various placeholders.

### List of used environment variables

You can specify the following environment variables in your project in order to autocomplete the license block.

* `TM_PROJECT_YEAR` or the current year
* `TM_PROJECT_COPYRIGHT_HOLDERS` or `TM_AUTHOR` or `TM_ORGANIZATION_NAME`
* `TM_ORGANIZATION_EMAIL`
* `TM_PROJECT_DESCRIPTION`

Also, you can fix your license project by adding the `TM_PROJECT_LICENSE` project environment variable. Thus,  you won't be required to select it again.

Malformed license block?
------------------------

It is possible that the license block rendering does not match your expectations. If this is the case, set your own format:

1. Bundles → Bundle Editor
2. In the **License Helper** entry, create a new Preference and set it up with the language's name
3. Fill the Scope Selector field with the appropriate scope – i.e. `source.java` for java source.
4. Set the shellVariables `TM_LICENSE_HELPER_HEADER` (comment start block) et `TM_LICENSE_HELPER_FOOTER` (comment end block) as following:

**Note :** you can also use the variable `TM_LICENSE_HELPER_LINE` to prefix each line of the license.

    {	shellVariables = (
    		{	name = 'TM_LICENSE_HELPER_HEADER';
    			value = '/*';
    		},
    		{	name = 'TM_LICENSE_HELPER_FOOTER';
    			value = '*/';
    		},
    	);
    }

Supported licenses
------------------

* [Affero GNU Public License 3.0](http://www.opensource.org/licenses/agpl-v3.html "GNU AFFERO GENERAL PUBLIC LICENSE v3 | Open Source Initiative")
* [Apache license 2.0](http://www.opensource.org/licenses/apache2.0.php "Open Source Initiative OSI - Apache License, Version 2.0:Licensing | Open Source Initiative")
* [CeCILL license](http://www.cecill.info/ "CeCILL")
* [Do What The Fuck You Want To Public License](http://sam.zoy.org/wtfpl/ "WTFPL - Do What The Fuck You Want To Public License")
* [GNU General Public License version 2](http://www.gnu.org/licenses/old-licenses/gpl-2.0.html "GNU General Public License v2.0 - GNU Project - Free Software Foundation (FSF)")
* [GNU General Public License version 3](http://www.gnu.org/licenses/gpl-3.0.html "The GNU General Public License - GNU Project - Free Software Foundation (FSF)")
* [GNU Lesser General Public License version 3](http://www.gnu.org/licenses/lgpl.html "GNU Lesser General Public License - GNU Project - Free Software Foundation (FSF)")
* [MIT license](http://www.opensource.org/licenses/mit-license.html "Open Source Initiative OSI - The MIT License:Licensing | Open Source Initiative")
* [New and Simplified BSD licenses](http://www.opensource.org/licenses/bsd-license.php "Open Source Initiative OSI - The BSD License:Licensing | Open Source Initiative")
* [Original BSD license](http://www.opensource.org/licenses/bsd-license.php "Open Source Initiative OSI - The BSD License:Licensing | Open Source Initiative")
* [PostgreSQL license](http://www.opensource.org/licenses/postgresql "The PostgreSQL Licence (TPL) | Open Source Initiative")

MIT License
-----------

Copyright (c) 2010 [Mehdi Kabab](http://pioupioum.fr/)

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.