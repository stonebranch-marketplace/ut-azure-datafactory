# Azure-DataFactory
Automation of Pipelines &amp; Triggers e.g., Run a Pipeline, start, stop a Trigger

<h1 style='margin: 30px 0px 0px; padding: 0px; color: rgb(23, 43, 77); font-size: 24px; line-height: 1.25; letter-spacing: -0.01em; font-weight: normal; text-transform: none; border-bottom-color: rgb(28, 57, 94); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; orphans: 2; text-align: start; text-indent: 0px; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>Introduction</h1>
<p style='margin: 10px 0px 0px; padding: 0px; color: rgb(23, 43, 77); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-size: 14px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>This Universal Task allows Stonebranch users to schedule, trigger, and monitor the Azure Data Factory pipeline process directly from Universal Controller. &nbsp;</p>
<h1 style='margin: 30px 0px 0px; padding: 0px; color: rgb(23, 43, 77); font-size: 24px; line-height: 1.25; letter-spacing: -0.01em; font-weight: normal; text-transform: none; border-bottom-color: rgb(28, 57, 94); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; orphans: 2; text-align: start; text-indent: 0px; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>Overview</h1>
<ul class="ak-ul" style='margin: 10px 0px 0px; list-style-type: disc; color: rgb(23, 43, 77); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-size: 14px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>
    <li>
        <p style="margin: 0px; padding: 0px;">This task uses&nbsp;Python modules azure-mgmt-resource and azure-mgmt-datafactory to make REST-API calls to Azure Data Factory.</p>
    </li>
    <li>
        <p style="margin: 0px; padding: 0px;">This task will use the Azure Tenant id, Subscription id, client id, client secret, Resource group, and location for authenticating the REST-API calls to Azure Data Factory.&nbsp;</p>
    </li>
    <li>
        <p style="margin: 0px; padding: 0px;">User can perform the following Azure Data Factory operations:</p>
        <ul class="ak-ul" style="margin: 0px; list-style-type: disc;">
            <li>
                <p style="margin: 0px; padding: 0px;">Run a Pipeline.&nbsp;</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">Get information on a Pipeline.</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">List all Pipelines.</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">Cancel Pipeline run.</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">List factory by resource group.</p>
            </li>
        </ul>
    </li>
    <li>
        <p style="margin: 0px; padding: 0px;">Also, with respect to Azure Data Factory triggers, users can perform the following operations from UAC:</p>
        <ul class="ak-ul" style="margin: 0px; list-style-type: disc;">
            <li>
                <p style="margin: 0px; padding: 0px;">Start Trigger.</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">Stop Trigger.</p>
            </li>
            <li>
                <p style="margin: 0px; padding: 0px;">List Trigger by Factory.</p>
            </li>
        </ul>
    </li>
    <li>
        <p style="margin: 0px; padding: 0px;">UAC also can restart a failed pipeline either from the failed step or from any activity name in the failed pipeline.</p>
    </li>
</ul>
<h1 style='margin: 30px 0px 0px; padding: 0px; color: rgb(23, 43, 77); font-size: 24px; line-height: 1.25; letter-spacing: -0.01em; font-weight: normal; text-transform: none; border-bottom-color: rgb(28, 57, 94); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; orphans: 2; text-align: start; text-indent: 0px; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>Software Requirements</h1>
<p style='margin: 10px 0px 0px; padding: 0px; color: rgb(23, 43, 77); font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; font-size: 14px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;'>This integration requires a Universal Agent and a Python runtime to execute the Universal Task against an Azure Data Factory.</p>

<p>&nbsp;</p>
Please visit this link to find key features, prerequisites, installation instructions, configuration instructions, and examples of how to use this integration. 
<a href="https://docs.stonebranch.com/confluence/display/UC69/UAC+-+Azure+Data+Factory">UAC - Azure Data Factory</a>.&nbsp;</li>
