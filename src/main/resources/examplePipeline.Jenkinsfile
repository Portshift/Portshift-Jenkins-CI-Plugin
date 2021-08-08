pipeline {
    agent any
    stages{
        stage ('secureCN') {
            steps {
                secureCNVulnerabilityScanner(imageName: 'registry.gitlab.com/repo/image:tag',
                  secureCnAccessKey: 'f5486ec2-7ba2-4e37-8aed-de700294bc76', secureCnSecretKeyId: 'secureCnSecretKey',
                  highestSeverityAllowed: 'HIGH', dockerRegistryPasswordId: 'GitlabCreds',
                  highestSeverityAllowedDf: 'FATAL', url: 'securecn.cisco.com', pushLocalImage: 'true')

            }
        }
    }
}