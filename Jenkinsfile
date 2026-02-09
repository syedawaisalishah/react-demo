pipline{
    agent any
    stages{
        environment {
            VERCEL_TOKEN=credentials("vercel_token")
        }
        stage("install"){
            steps{
                bat "npm install"
            }
        }
        stage("build"){
            steps{
             bat "npm run build"
            }
        }
        stage("deploy"){
            steps{
                bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}