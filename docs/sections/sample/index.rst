.. This is a comment. Note how any initial comments are moved by
   transforms to after the document title, subtitle, and docinfo.

.. demo.rst from: http://docutils.sourceforge.net/docs/user/rst/demo.txt

.. |EXAMPLE| image:: static/yi_jing_01_chien.jpg
   :width: 1em

**********************
Demo Data
**********************

.. contents:: Table of Contents
Overview
==================

Quail contains 5 Demo Stores and 5 Demo Layers

Demo QGIS Stores
=================

QGIS Stores are QGIS Projects with any required flat files.

The QGIS Demo Stores are below

.. image:: demo-stores-1.png

**BGS-GeoPackage.** Geopackage data source obtained from the British Geological Survey.

**Chicago-ESRI-Shapefile.** - ESRI Shapefile data source obtained from the Chicago Data Portal

**Gebco-WMS.** - WMS source obtained from GEBCO

**Monarch-ESRI-Geodatabase.** ESRI Geodatabase data source for Monarch butterfly habitat

**NASA-GeoTIFF.** GeoTiff data source from NASA showing percipitation

**USA-PostGIS.**  PostGIS data source using the GeoServer USA Population data


Demo PostGIS Stores
=================

The installation contains a Demo PostGIS Store

.. image:: postgis-demo-store.png

This Store is created from a PostGIS database that is installed with Quail.

It is used in the USA Layer demo.


Demo QGIS Layers
================

QGIS Layers are Layers created from QGIS Stores.

The QGIS Demo Layers are below

.. image:: demo-layers.png

The Layer lists the Store from which it was created.

It also lists which layers from the QGIS Project will be included in the Layer.


Demo Layer
================

 
States Database
================

The sample database, states, contains the data for the PostGIS Store, usdata::

     states=# \dt
               List of relations
     Schema  |      Name       | Type  |  Owner
   ----------+-----------------+-------+----------
    public   | spatial_ref_sys | table | qgapp
    public   | states          | table | qgapp
    topology | layer           | table | qgapp
    topology | topology        | table | qgapp
   (4 rows)



Sample Data Source
================

The included sample Data Source is a JNDI connection to the beedatabase:

layer-sample-chicago.png

.. image:: layer-sample-chicago.png


layer-sample-data.png

.. image:: layer-sample-data.png

layer-sample-neighborhoods.png


.. image:: layer-sample-neighborhoods.png

layer-sample-states.png


.. image:: layer-sample-states.png


layer-sample-usa.png

.. image:: layer-sample-usa.png

layers-sample-1.png

.. image:: layers-sample-1.png


layers-sample-2.png

.. image:: layers-sample-2.png


postgis-sample-1.png

.. image:: postgis-sample-1.png


qlayersdashboard.png

.. image:: qlayersdashboard.png


stores-sample-1.png

.. image:: stores-sample-1.png

stores-sample-2.png

.. image:: stores-sample-2.png

stores-sample-3.png

.. image:: stores-sample-3.png


stores-sample-4.png



Sample Reports
================

Three Sample Reports are created

* Simple Bee Report	- this is a basic chart report

.. image:: ../../_static/simple-bee-report.png


* LOV Parameter - This is a basic report using a single LOV (List of Values) Parameter

.. image:: ../../_static/lov-report-0.png


* Query Parameter - This is a basic report using two Query Parameters

.. image:: ../../_static/query-report-3.png


Change From:

      const wmsLayer = L.tileLayer.wms('proxy_qgis.php?', {
		   layers: '<?=implode(',', QGIS_LAYERS)?>'
	   }).addTo(map);

Change to::

      const wmsLayer = L.tileLayer.wms('/mproxy/service', {
       layers: 'neighborhoods'
	   }).addTo(map);



Sample Schedules
================

A sample Schedule is created for each report.

Note: These Schedules, do not have email activated.  You can edit them to include email delivery to test email functionality.

.. image:: ../../_static/sample-schedule.png



Sample Parameters
=====================

Sample Parameters are include for the LOV Parameter and Query Parameter reports

.. image:: ../../_static/sample-parameter.png

Delete Sample Data
===================

To delete the sample data:

1. Delete Sample Schedules
2. Delete Sample Reports
3. Delete Sample Data Sources
4. Drop beedatabase



