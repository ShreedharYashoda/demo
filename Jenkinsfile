def executeWithMask (cmd, label) { 
	sh script: '#/bin/sh -e \n' + cmd,
					label: label
}

def artifactoryToken

pipeline {
	agent any

	triggers {
		GenericTrigger(
			genericVariables: [
					[key: 'ref', value: '$.ref']
				],

I			causeString: 'Triggered on $ref',

			token: 'deliverywindowservicedeveloptoken',
			tokenCredentialId: '',

			printContributedVariables: true,
			printPostContent: true,

			silentResponse: false,

			regexpFilterText: '$ref',
			regexpFilterExpression: 'refs/heads/master'
