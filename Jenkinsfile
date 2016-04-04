plumber([
        scm: [
                [
                        name: 'git',
                        config: [
                                url: "git://github.com/abayer/pipeline-action-plugin.git",
                                branch: "origin/master"
                        ]
                ]
        ],

        archiveDirs: "target/**",

        phases: [
                [
                        name: "run-maven",
                        action: [
                                name: "plumberMvnDemo",
                                mavenVersion: "maven3.3.3",
                                javaVersion: "java8",
                                goals: "clean install"
                        ]
                ]
        ],
        debug: true

])