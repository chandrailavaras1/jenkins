pipeline{
    agent any
    parameters{
        string(
            name: "USR_NAME",
            defaultValue: "Chandu",
            description: "Do enter your name"
        )
        booleanParam(
            name: "SRE_APPROVED",
            defaultValue: true,
            description: "Is SRE approval taken for this release..?"
        )
        choice(
            choices: 'Regular\nHotfix',
            description: "What sort of release is this, regulare release or hotfix ?",
            name: 'Release'
        )
        text(
            name: "Notes",
            defaultValue: "Sample Text",
            description: "Do enter text"
        )
        credentials(
            name: "My credentials",
            required: true,
            description: "MY Credentials"
        )
    }
    stages{
        stage("Sample build"){
            steps{
                echo "Sample build"
                echo "Welcome ${params.USR_NAME}"
            }
        }
    }
}
