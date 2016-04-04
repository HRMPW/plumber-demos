plumber([
        env: ["ANIMAL": "chicken"],
        
        phases: [
            [
                name: "first-phase",
                stashDirs: "names.txt"
                action: [
                        script: 'echo "I am stashing my file"'
                ]
            ],

            [
                name: "split-phases-1",
                skipSCM: true,
                unstash: "first-phase",
                action: [
                    name: "plumberAnimal",
                    animal: "walrus"
                ],
                after: "first-phase"
            ],

            [
                name: "split-phases-2",
                skipSCM: true,
                unstash: "first-phase",
                action: [
                    name: "plumberAnimal",
                    animal: "cheetah"
                ],
                after: "first-phase"
            ],

            [
                name: "joined-phase",
                skipSCM: true,
                unstash: "first-phase",
                action: [
                    name: "plumberAnimal",
                    animal: "hippo"
                ],
                after: ["split-phases-1", "split-phases-2"]
            ]
        ],
        debug: true
])
