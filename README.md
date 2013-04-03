This is an Emmet extension that allows the user to create Visualforce page skeleton in addition to HTML, CSS etc.

For example the following line of code -

    ap:pg>ap:pb>ap:pbt[value="{!mAccountList}"  var="x"]>ap:col[value='{!x.}']*5

will create Visualforce code as shown below

    <apex:page>
        <apex:pageBlock title="">
        		<apex:pageBlockTable value="{!mAccountList}" var="x">
          			<apex:column value="{!x.}"></apex:column>
          			<apex:column value="{!x.}"></apex:column>
          			<apex:column value="{!x.}"></apex:column>
          			<apex:column value="{!x.}"></apex:column>
          			<apex:column value="{!x.}"></apex:column>
        		</apex:pageBlockTable>
      	</apex:pageBlock>
    </apex:page>

