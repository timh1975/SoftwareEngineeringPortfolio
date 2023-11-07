
## Issue

I took on the issue that dealt with storing information on equipment.  Looking at the ERD, there are three tables that relate to this.
  1.  Equipmennt.  This table stores information on each piece of equipment.
  2.  Equipment_Type. This table stores a list of equipment categories
  3.  Equipment_Allocation.  This table stores information on where and when equipment is allocated

## Maintaining agreed architecture

My code base followed the following code architecture. This was decided by the group after undertaking the ToDoList example.

  1.  Database class for CRUD operations was added to the Data folder
  2.  The table structures were added to the models folder
  3.  The views and their underlying code were added to the Views folder.

The table structures were added to the models architucture. The example below (fig 1) is for the Equipment Allocation table.  The knowledge gained from last week was applied in the method of adding a foreign key.  Furthermore, I learnt that SQLite does not use the DATE data structure, ratht that the dates are stored in strings.

![](/images/week9-add-model.png "")

**fig 1 (Equipment Table model)**

A seperate database class was created to store the CRUD functions for the Equipment related tables.  In figure 2, the InitiateDataBase method creates a new local database if it does not already exists 

![](/images/week9-add-initiate.png "")
  
**fig 2 (Initiate Database and tables)**

The code below shows 2 CRUD methods in the database class. They have comments placed on top to add Doxygen documents, have single responsbility and short.  Improvments would include changing the name strings in line 80 to something more meaningfull, such as names_returned. The SQL statement for the GetEquipment method is vulnerable to SQL injection attacks as the serach query is embedded in the statement.  Given the scope of this project, it was decided not to add protection this week. However, this is something I will learn and implement in future projects. 

There are three seperate views for the graphical interface which was added to the view model. A equipment UI was created with three buttons: add equipment type, add equipment and allocate equipment.

Error capturing was added to the Add Equipment Page. Fig 3 shows an error message when data fields are null prior to saving.  Fig 4 shows the code that validates user input by checking if the editor boxes is null. If so, it returns false.

Fig 4 shows how the error capture is handled if the validation is false, by the use of a condition. If it is false, a error message will apear as in fig 3, otherwise it will save the record

![](/images/week9-error-capture.png "")

**fig 3(Error capturing)**

![](/images/week9-validate-date.png "")

**fig 4(Validate user input method)**

![](/images/week9-error-capture-in-method.png "")

**fig 5(Error capture handling in AddEquipment method)**


## Code Review

I undertook the code view (fig 6). Whilst most of the code was clean, it did lack comments and some lines of code was commented out.  I provided this in a feedback (fig 7)
and requested for changes.

![](/images/week9-code-review-example.png "")

**fig 6 (Code Review Example)**

![](/images/week9-code=review-feedback.png "")

**fig 7(Review feedback)**

## Documentation

Documentation was undertaken using Doxygen and added to the Document folder in the repo.  Fig 7 is an example


<body>
<div id="top"><!-- do not remove this div, it is closed by doxygen! -->
<div id="titlearea">
<table cellspacing="0" cellpadding="0">
 <tbody>
 <tr id="projectrow">
  <td id="projectalign">
   <div id="projectname">My Project
   </div>
  </td>
 </tr>
 </tbody>
</table>
</div>

</script>
<script type="text/javascript" src="menudata.js"></script>
<script type="text/javascript" src="menu.js"></script>
<script type="text/javascript">
/* @license magnet:?xt=urn:btih:d3d9a9a6595521f9666a5e94cc830dab83b65699&amp;dn=expat.txt MIT */
$(function() {
  initMenu('',true,false,'search.php','Search');
  $(document).ready(function() { init_search(); });
});
/* @license-end */
</script>
<div id="main-nav"></div>
<!-- window showing the filter options -->
<div id="MSearchSelectWindow"
     onmouseover="return searchBox.OnSearchSelectShow()"
     onmouseout="return searchBox.OnSearchSelectHide()"
     onkeydown="return searchBox.OnSearchSelectKey(event)">
</div>

<!-- iframe showing the search results (closed by default) -->
<div id="MSearchResultsWindow">
<div id="MSearchResults">
<div class="SRPage">
<div id="SRIndex">
<div id="SRResults"></div>
<div class="SRStatus" id="Loading">Loading...</div>
<div class="SRStatus" id="Searching">Searching...</div>
<div class="SRStatus" id="NoMatches">No Matches</div>
</div>
</div>
</div>
</div>

<div id="nav-path" class="navpath">
  <ul>
<li class="navelem"><a class="el" href="namespace_u_n_d_a_c___project.html">UNDAC_Project</a></li><li class="navelem"><a class="el" href="namespace_u_n_d_a_c___project_1_1_data.html">Data</a></li><li class="navelem"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html">EquipmentDB</a></li>  </ul>
</div>
</div><!-- top -->
<div class="header">
  <div class="summary">
<a href="#pub-static-methods">Static Public Member Functions</a> &#124;
<a href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b-members.html">List of all members</a>  </div>
  <div class="headertitle"><div class="title">UNDAC_Project.Data.EquipmentDB Class Reference</div></div>
</div><!--header-->
<div class="contents">
<table class="memberdecls">
<tr class="heading"><td colspan="2"><h2 class="groupheader"><a id="pub-static-methods" name="pub-static-methods"></a>
Static Public Member Functions</h2></td></tr>
<tr class="memitem:a001f8bb2339f7fdf822c02a99408aa3d" id="r_a001f8bb2339f7fdf822c02a99408aa3d"><td class="memItemLeft" align="right" valign="top">static async Task&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#a001f8bb2339f7fdf822c02a99408aa3d">InitiateDataBase</a> ()</td></tr>
<tr class="memdesc:a001f8bb2339f7fdf822c02a99408aa3d"><td class="mdescLeft">&#160;</td><td class="mdescRight">Check if local database exists. Creates new one with table if it does not exist.  <br /></td></tr>
<tr class="separator:a001f8bb2339f7fdf822c02a99408aa3d"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:ad24e052d04b226e093c70e4bc75a3763" id="r_ad24e052d04b226e093c70e4bc75a3763"><td class="memItemLeft" align="right" valign="top">static async Task&lt; int &gt;&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#ad24e052d04b226e093c70e4bc75a3763">GetEquipmentTypeForeignKey</a> (string eType)</td></tr>
<tr class="memdesc:ad24e052d04b226e093c70e4bc75a3763"><td class="mdescLeft">&#160;</td><td class="mdescRight">Gets equipment type id number.  <br /></td></tr>
<tr class="separator:ad24e052d04b226e093c70e4bc75a3763"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:adca741ab12d7bbcfb64dfae634fa8cf6" id="r_adca741ab12d7bbcfb64dfae634fa8cf6"><td class="memItemLeft" align="right" valign="top">static async Task&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#adca741ab12d7bbcfb64dfae634fa8cf6">ListEquipment</a> (<a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a> eq)</td></tr>
<tr class="memdesc:adca741ab12d7bbcfb64dfae634fa8cf6"><td class="mdescLeft">&#160;</td><td class="mdescRight">Add Equipment to database.  <br /></td></tr>
<tr class="separator:adca741ab12d7bbcfb64dfae634fa8cf6"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:a54cd4ae39c0bf9de2d5c958c162aab33" id="r_a54cd4ae39c0bf9de2d5c958c162aab33"><td class="memItemLeft" align="right" valign="top">static async Task&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#a54cd4ae39c0bf9de2d5c958c162aab33">AddEquipment</a> (<a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a> eq)</td></tr>
<tr class="memdesc:a54cd4ae39c0bf9de2d5c958c162aab33"><td class="mdescLeft">&#160;</td><td class="mdescRight">Add Equipment to database.  <br /></td></tr>
<tr class="separator:a54cd4ae39c0bf9de2d5c958c162aab33"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:a38c505a4254732379c44ac28e1fa03b0" id="r_a38c505a4254732379c44ac28e1fa03b0"><td class="memItemLeft" align="right" valign="top">static async Task&lt; string[]&gt;&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#a38c505a4254732379c44ac28e1fa03b0">GetEquipmentType</a> ()</td></tr>
<tr class="memdesc:a38c505a4254732379c44ac28e1fa03b0"><td class="mdescLeft">&#160;</td><td class="mdescRight">Return list of equipment types from database.  <br /></td></tr>
<tr class="separator:a38c505a4254732379c44ac28e1fa03b0"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:abe4f0930c99c7b94ae96f3c4b41011f6" id="r_abe4f0930c99c7b94ae96f3c4b41011f6"><td class="memItemLeft" align="right" valign="top">static async Task&lt; List&lt; <a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a> &gt; &gt;&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#abe4f0930c99c7b94ae96f3c4b41011f6">GetEquipment</a> (string name)</td></tr>
<tr class="memdesc:abe4f0930c99c7b94ae96f3c4b41011f6"><td class="mdescLeft">&#160;</td><td class="mdescRight">Return list of equipment from database based the the search condition of equipment name.  <br /></td></tr>
<tr class="separator:abe4f0930c99c7b94ae96f3c4b41011f6"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:a7d541ad863f2285eba44b968e7d8c003" id="r_a7d541ad863f2285eba44b968e7d8c003"><td class="memItemLeft" align="right" valign="top">static async Task&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#a7d541ad863f2285eba44b968e7d8c003">AddEquipmentAllocation</a> (<a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment___allocation.html">Equipment_Allocation</a> ea)</td></tr>
<tr class="memdesc:a7d541ad863f2285eba44b968e7d8c003"><td class="mdescLeft">&#160;</td><td class="mdescRight">Add equipment allocation to database.  <br /></td></tr>
<tr class="separator:a7d541ad863f2285eba44b968e7d8c003"><td class="memSeparator" colspan="2">&#160;</td></tr>
<tr class="memitem:ad429e890abc0565b8641072f3ce3c9df" id="r_ad429e890abc0565b8641072f3ce3c9df"><td class="memItemLeft" align="right" valign="top">static async Task&#160;</td><td class="memItemRight" valign="bottom"><a class="el" href="class_u_n_d_a_c___project_1_1_data_1_1_equipment_d_b.html#ad429e890abc0565b8641072f3ce3c9df">AddEquipmentType</a> (<a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment__type.html">Equipment_type</a> et)</td></tr>
<tr class="memdesc:ad429e890abc0565b8641072f3ce3c9df"><td class="mdescLeft">&#160;</td><td class="mdescRight">Add Equipment type to database.  <br /></td></tr>
<tr class="separator:ad429e890abc0565b8641072f3ce3c9df"><td class="memSeparator" colspan="2">&#160;</td></tr>
</table>
<a name="details" id="details"></a><h2 class="groupheader">Detailed Description</h2>
<div class="textblock">
<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00008">8</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>
</div><h2 class="groupheader">Member Function Documentation</h2>
<a id="a54cd4ae39c0bf9de2d5c958c162aab33" name="a54cd4ae39c0bf9de2d5c958c162aab33"></a>
<h2 class="memtitle"><span class="permalink"><a href="#a54cd4ae39c0bf9de2d5c958c162aab33">&#9670;&#160;</a></span>AddEquipment()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task UNDAC_Project.Data.EquipmentDB.AddEquipment </td>
          <td>(</td>
          <td class="paramtype"><a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a>&#160;</td>
          <td class="paramname"><em>eq</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Add Equipment to database. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">eq</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00063">63</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="a7d541ad863f2285eba44b968e7d8c003" name="a7d541ad863f2285eba44b968e7d8c003"></a>
<h2 class="memtitle"><span class="permalink"><a href="#a7d541ad863f2285eba44b968e7d8c003">&#9670;&#160;</a></span>AddEquipmentAllocation()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task UNDAC_Project.Data.EquipmentDB.AddEquipmentAllocation </td>
          <td>(</td>
          <td class="paramtype"><a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment___allocation.html">Equipment_Allocation</a>&#160;</td>
          <td class="paramname"><em>ea</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Add equipment allocation to database. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">ea</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00108">108</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="ad429e890abc0565b8641072f3ce3c9df" name="ad429e890abc0565b8641072f3ce3c9df"></a>
<h2 class="memtitle"><span class="permalink"><a href="#ad429e890abc0565b8641072f3ce3c9df">&#9670;&#160;</a></span>AddEquipmentType()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task UNDAC_Project.Data.EquipmentDB.AddEquipmentType </td>
          <td>(</td>
          <td class="paramtype"><a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment__type.html">Equipment_type</a>&#160;</td>
          <td class="paramname"><em>et</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Add Equipment type to database. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">et</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00120">120</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="abe4f0930c99c7b94ae96f3c4b41011f6" name="abe4f0930c99c7b94ae96f3c4b41011f6"></a>
<h2 class="memtitle"><span class="permalink"><a href="#abe4f0930c99c7b94ae96f3c4b41011f6">&#9670;&#160;</a></span>GetEquipment()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task&lt; List&lt; <a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a> &gt; &gt; UNDAC_Project.Data.EquipmentDB.GetEquipment </td>
          <td>(</td>
          <td class="paramtype">string&#160;</td>
          <td class="paramname"><em>name</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Return list of equipment from database based the the search condition of equipment name. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">name</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00095">95</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="a38c505a4254732379c44ac28e1fa03b0" name="a38c505a4254732379c44ac28e1fa03b0"></a>
<h2 class="memtitle"><span class="permalink"><a href="#a38c505a4254732379c44ac28e1fa03b0">&#9670;&#160;</a></span>GetEquipmentType()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task&lt; string[]&gt; UNDAC_Project.Data.EquipmentDB.GetEquipmentType </td>
          <td>(</td>
          <td class="paramname"></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Return list of equipment types from database. </p>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00074">74</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="ad24e052d04b226e093c70e4bc75a3763" name="ad24e052d04b226e093c70e4bc75a3763"></a>
<h2 class="memtitle"><span class="permalink"><a href="#ad24e052d04b226e093c70e4bc75a3763">&#9670;&#160;</a></span>GetEquipmentTypeForeignKey()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task&lt; int &gt; UNDAC_Project.Data.EquipmentDB.GetEquipmentTypeForeignKey </td>
          <td>(</td>
          <td class="paramtype">string&#160;</td>
          <td class="paramname"><em>eType</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Gets equipment type id number. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">eType</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd>Foreign Key</dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00038">38</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="a001f8bb2339f7fdf822c02a99408aa3d" name="a001f8bb2339f7fdf822c02a99408aa3d"></a>
<h2 class="memtitle"><span class="permalink"><a href="#a001f8bb2339f7fdf822c02a99408aa3d">&#9670;&#160;</a></span>InitiateDataBase()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task UNDAC_Project.Data.EquipmentDB.InitiateDataBase </td>
          <td>(</td>
          <td class="paramname"></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Check if local database exists. Creates new one with table if it does not exist. </p>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00019">19</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<a id="adca741ab12d7bbcfb64dfae634fa8cf6" name="adca741ab12d7bbcfb64dfae634fa8cf6"></a>
<h2 class="memtitle"><span class="permalink"><a href="#adca741ab12d7bbcfb64dfae634fa8cf6">&#9670;&#160;</a></span>ListEquipment()</h2>

<div class="memitem">
<div class="memproto">
<table class="mlabels">
  <tr>
  <td class="mlabels-left">
      <table class="memname">
        <tr>
          <td class="memname">static async Task UNDAC_Project.Data.EquipmentDB.ListEquipment </td>
          <td>(</td>
          <td class="paramtype"><a class="el" href="class_u_n_d_a_c___project_1_1_models_1_1_equipment.html">Equipment</a>&#160;</td>
          <td class="paramname"><em>eq</em></td><td>)</td>
          <td></td>
        </tr>
      </table>
  </td>
  <td class="mlabels-right">
<span class="mlabels"><span class="mlabel">static</span></span>  </td>
  </tr>
</table>
</div><div class="memdoc">

<p>Add Equipment to database. </p>
<dl class="params"><dt>Parameters</dt><dd>
  <table class="params">
    <tr><td class="paramname">eq</td><td></td></tr>
  </table>
  </dd>
</dl>
<dl class="section return"><dt>Returns</dt><dd></dd></dl>

<p class="definition">Definition at line <a class="el" href="_equipment_d_b_8cs_source.html#l00051">51</a> of file <a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a>.</p>

</div>
</div>
<hr/>The documentation for this class was generated from the following file:<ul>
<li>UNDAC Project/Data/<a class="el" href="_equipment_d_b_8cs_source.html">EquipmentDB.cs</a></li>
</ul>
</div><!-- contents -->
<!-- start footer part -->
<hr class="footer"/><address class="footer"><small>
Generated by&#160;<a href="https://www.doxygen.org/index.html"><img class="footer" src="doxygen.svg" width="104" height="31" alt="doxygen"/></a> 1.9.8
</small></address>
</body>
</html>

**fig 7(Documentation fo the EquipmentDB database class)**

## Reflection

The following reflections were made from this portfolio

1.  There could be a debate of having a database class for each of the equipment related tables. However, it was decided to keep them in one database class using the following that the InitateDataBase function creates all related equipoment tables. This was decided to do this in one function given that they are linked with foreign keys. This was to minimise the risk of tables not being created properly if a foreign key does not yet reference an existing table.  Furthermore, given that there were only 8 methods, it was decided that this was not too much for one class.
   
2. Whilst using a local database in the early development, I have recognise that this is problematic in the following ways
     2.1  There is the requirement for features to be merged into the development branch in order to sync the local database with changes due to added tables.
     2.2  Datasets would need to be provded to be added to the local database to sync up data.
     2.3  Not having a fully sync database would provide difficulty in testing for system wide compatability.

3.  No unit tesing was put in place. I was able to figure out using mock tests for this week. This is an area I recognise I need to gain knowledge and skilsl on for both the project module for semester 2, as well as for professional practice.
4.  Given that SQL injection vulnerability was recognised, I would need to read up on optimising SQL statments to mitigate for these risks.  
