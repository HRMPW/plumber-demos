plumber([
        
        phases: [
            [
                name: "first-phase",
                stashDirs: "animal.txt",
                action: [
                        script: 'echo "I am stashing my file";echo "tiger" >> animal.txt'
                ]
            ],
            [
                name: "joined-phase",
                skipSCM: true,
                unstash: "first-phase",
                action: [
                    name: "plumberAnimal",
                    animal: "hippo"
                ],
                after: ["split-phases-1"]
            ],

            [
                name: "split-phases-1",
                skipSCM: true,
                unstash: "first-phase",
                stashDirs: "animal.txt"
                action: [
                    name: "plumberAnimal",
                    animal: "walrus"
                ],
                after: "first-phase"
            ]
            
        ],
        debug: true
])
