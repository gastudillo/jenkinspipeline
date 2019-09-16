#!groovy

def isMaster = env.BRANCH_NAME == "master"

def settings = isMaster ? EnvSettings.PROD : EnvSettings.STAGE

stage("Running") {

    echo 'test ' + env.BRANCH_NAME

    echo settings.cron
}

enum EnvSettings {
    PROD(
      "0 13 * * 1-5"
    ),
    STAGE(
      ""
    );

    String cron

    EnvSettings(
      String cron
    ) {
      this.cron = cron
    }

}