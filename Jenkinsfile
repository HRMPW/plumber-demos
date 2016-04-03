plumber([
        phases: [
                [
                        name: "first-phase",
                        action: [
                                script: "echo 'Hey look, running'"
                        ]
                ],
                [
                        name: "input-phase",
                        action: [
                                name: "input",
                                message: "Continue to next phase?",
                                ok: "Yup, continue!"
                        ],
                        after: "first-phase"
                ],
                [
                        name: "last-phase",
                        action: [
                            script: "echo 'Got to last phase."
                        ],
                        after: "input-phase"
                ]
        ],
        debug: true

])