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
            name: "Release",
            defaultValue: "Regular\nHotfix",
            description: "What is the release hotfix/release...?"
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
