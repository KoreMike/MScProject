# MScProject

*Files to edit*

autocomplete-master/solr-home/ac/conf/velocity/suggest.vm

Change line 18 to $d.textsuggest so that autocomplete query works

autocomplete-master/solr-home/ac/conf/velocity/doc.vm

Configured second column in result to show the url link (as picked up from the 'value' column in the csv:
'''
<td>
#if($doc.getFieldValue('thumbnail_url') != "")
<img src="#field('thumbnail_url')"/>
#end
#if($doc.getFieldValue('value') != "")
<div><a href="#field('value')">link</a></div>
#end
</td>
'''
