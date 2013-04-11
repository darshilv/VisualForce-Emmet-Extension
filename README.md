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
    
# Other Examples

    ap:pg[controller="EmmetDemoController"]>ap:pb[title="Account List"]>ap:pbt[value="{!mAccountList}"    var="x"]>ap:col[value="{!x.}"]*5
    
    ap:pb[title="{!Account.Name}"]>ap:pbs[columns="2"]>(ap:pbsi>ap:of[value={!Account}])*5

To install this extension please follow the instructions here:

    https://github.com/darshilv/VisualForce-Emmet-Extension/blob/master/Installation_Instructions.md

# Licence

    Copyright (c) 2013, salesforce.com, Inc.
    All rights reserved.
    
    Redistribution and use in source and binary forms, with or without modification, 
    are permitted provided that the following conditions are met:
    
        * Redistributions of source code must retain the above copyright notice, 
        this list of conditions and the following disclaimer.
        * Redistributions in binary form must reproduce the above copyright notice, 
        this list of conditions and the following disclaimer in the documentation 
        and/or other materials provided with the distribution.
        * Neither the name of the salesforce.com, Inc. nor the names of its contributors 
        may be used to endorse or promote products derived from this software 
        without specific prior written permission.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND 
    ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED 
    WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. 
    IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, 
    INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, 
    BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
    DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF 
    LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE 
    OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED 
    OF THE POSSIBILITY OF SUCH DAMAGE.
