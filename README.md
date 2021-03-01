<p><strong>Azure Data Factory &ndash; UAC Integration</strong><span data-preserver-spaces="true">&nbsp;</span></p>
<p><span data-preserver-spaces="true">This Universal Task allows Stonebranch users to schedule, trigger &amp; monitor the Azure Data Factory pipeline process directly from the Universal Controller.&nbsp;&nbsp;</span></p>
<p><strong>Key Features:</strong><span data-preserver-spaces="true">&nbsp;</span></p>
<ul>
<li><span data-preserver-spaces="true">This task uses python modules azure-mgmt-resource &amp; azure-mgmt-datafactory to make REST-API calls to Azure Data Factory</span></li>
<li><span data-preserver-spaces="true">This task will use the Azure Tenant id, Subscription id, client id, client secret, Resource group &amp; location for authenticating the REST-API calls to Azure Data Factory.&nbsp;</span></li>
<li><span data-preserver-spaces="true">Users can perform the below Azure Data Factory operations.</span></li>
<ul>
<li class="ql-indent-1"><span data-preserver-spaces="true">Run a Pipeline&nbsp;</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">Get a Pipeline info</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">List all Pipelines</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">Cancel Pipeline run</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">List factory by resource group</span></li>
</ul>
<li><span data-preserver-spaces="true">Azure Data Factory triggers user can perform the below operations from UAC:</span></li>
<ul>
<li class="ql-indent-1"><span data-preserver-spaces="true">Start Trigger</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">Stop Trigger</span></li>
<li class="ql-indent-1"><span data-preserver-spaces="true">List Trigger by Factory</span></li>
</ul>
<li><span data-preserver-spaces="true">UAC also can restart a failed pipeline either from the failed step or from any activity name in the failed pipeline</span></li>
</ul>
<p>&nbsp;</p>

<p>&nbsp;</p>
Please visit this link to find key features, prerequisites, installation instructions, configuration instructions, and examples of how to use this integration. 
<a href="https://docs.stonebranch.com/confluence/display/UC69/UAC+-+Azure+Data+Factory">UAC - Azure Data Factory</a>.&nbsp;</li>
