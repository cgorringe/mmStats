README
------

mmStats 12/11/2011 <br/>
by Carl Gorringe <car1@gorringe.org>

### mmtop10.pl ###

This script downloads from a Mailman mailing list archive at the given URL, then outputs the Top-10 users by number of posts in each month, and the overall total.


Installation
------------

Perl is required to run this program.

Next you may need to install the `IO::Socket::SSL` module if you are reading from any website that uses https.  This module isn't normally part of the core Perl install.  We can install this from the CPAN repository by typing the following from a Linux terminal:

    sudo perl -MCPAN -e 'install IO::Socket::SSL'

If this is the first time using CPAN on your system, it will prompt you to set up CPAN first.  The default settings should work fine.


How To Use
----------

From a Linux terminal, use the following syntax:

    ./mmtop10.pl URL > output.html

Where you should replace URL with the address of the mailing list archive page.

For example:

    ./mmtop10.pl https://www.noisebridge.net/pipermail/noisebridge-discuss/ > top10.html

Then place the `mmstyle.css` stylesheet file in to the same directory as your html file.  Load the html in a browser and you're done.  Feel free to modify the stylesheet or edit the html to your liking.


### Tips ###

*  To make permanent changes to the HTML created from the Perl script, try modifing the `htmlHeader()` and `htmlFooter()` subroutines in the `mmtop10.pl` file.

*  To create a dynamically changing Top-10 page every month, try running the script from a cron job on the first day of the month every month.



