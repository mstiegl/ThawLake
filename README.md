Thaw Lake Model
===============

This model a 1-D numerical model of permafrost and subsidence processes.
It aims to investigate the subsurface thermal impact of thaw lakes of
various depths, and to evaluate how this impact might change in a warming
climate.  

The model was designed for the Alaskan Arctic Coastal Plain
and uses average and amplitude of temperature from observed permafrost
temperatures at 5cm in the subsurface at Drew Point data (USGS)
in 1-D, subsurface temperature changes through time and space of a
semi-infinite half-space, then plots the result.  The model code incorporates
phase change by using the apparent heat capacity scheme for temperatures
within the "phase-change envelope".  

lake-permafrost model - lake freezes and thaws, permafrost changes temperature,
when permafrost thaw it subsides, assuming that if excess ice melts all 
the water leaves the permafrost and thus the subsurface volume decreases.  

boundary condition of ice bottom and lake water top = Tf
  if Ts<Tf, top boundary condition for calculation is Ts.
  if Ts>Tf, top boundary condition --> Tf and excess energy is used
     to melt ice.

When ice melted from the top, all other boundary just moved up by equivelant
amount, if moved up a full control volume then bottom control volume
added that is same temp as (end-1) control volume.  Assumes that when ice
free, lake is completely mixed.  (ie Liston & Hall)


Primary reference: Matell, N., Anderson, R.S., Overeem, I., Wobus, C.,
Urban, F., Clow, G., 2013 Modeling the subsurface thermal impact of Arctic
thaw lakes in a warming climate. Computers and Geosciences. 
 
Additional reference: Clow, G.D., 2008a. Continued permafrost warming in
northern Alaska, 2008 update. NOAA/ESRL Global Monitoring Annual Conference,
Boulder.  

The model uses observed heat flow for thermal gradient from:
Lachenbruch, A.H., Sass, J.H., Marshall, B.V., Moses, T.H., Jr., 1982.
Temperatures, heat flow, and the geothermal regime at Prudhoe Bay, Alaska.
Journal of Geophysical Research 87, 9301-9316.  

This version is written for Python 2.6+


Originates from earlier code by Nora Matell and co-authors.
Copyright to Python version  (C) <2017> <Irina Overeem, Montek Singh>

Developer can be contacted by irina.overeem@colorado.edu

Dr. Irina Overeem
CSDMS Community Surface Dynamics Modeling System
INSTAAR, University of Colorado at Boulder
PO Box 450, 80309-0450
Boulder, CO, USA

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA. 


Usage:
======

Clone this repository

Ensure Python 2 is in use

cd thalake/

python thalake.py


Expected output:

    hello maybe this is working
    1
    else loop
    Maybe Elif it is
    253
    thalake.py:449: VisibleDeprecationWarning: using a non-integer number instead of an integer will result in an error in the future
      depthsubsidenew = self.z[numthawedspec]*self.excessice;
    had to adjust
    2
    else loop
    Maybe Elif it is
    253
    had to adjust
    3
    else loop
    Maybe Elif it is
    253
    had to adjust
    4
    else loop
    Maybe Elif it is
    253
    had to adjust
    5
    else loop
    Maybe Elif it is
    253
    had to adjust
    Loop ended

Imminently Needed Improvements:
-------------------------------

* Restructure code as a proper Python package
* Clean up output statements
* Describe input and output
* Provide plotting guidance to users
