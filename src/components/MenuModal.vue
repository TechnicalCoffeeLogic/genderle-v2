<script setup>

</script>

<template>

    <div class="modal fade" id="helpModal" tabindex="-1" aria-labelledby="helpModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-scrollable">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="helpModalLabel">Help</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="accordion" id="accordionHelp">
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingOne">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                    How To Play GENDERLE
                                </button>
                            </h2>
                            <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                                data-bs-parent="#accordionHelp">
                                <div class="accordion-body">
                                    <strong>How To Play:</strong> Determine the correct gender of the person in the
                                    picture that is presented to you. You will get five tries to figure out the correct
                                    gender, your guess can have blank spaces in them, that means you do not have to fill
                                    out the entire 6 squares. <br /><br />
                                    <ul>
                                        <li>
                                            <i class="bi bi-square-fill" style="color:rgb(83,141, 78);"></i> A green
                                            square means you have the correct letter in the correct position.
                                        </li>
                                        <li>
                                            <i class="bi bi-square-fill" style="color:rgb(181, 159, 59);"></i> A yellow
                                            square means you have the correct letter, but in the wrong postition of the
                                            word.
                                        </li>
                                        <li>
                                            <i class="bi bi-square-fill" style="color:rgb(58, 58, 60);"></i> A gray
                                            sqaure means that the letter does not exist in the answer.
                                        </li>
                                    </ul>

                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingTwo">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                    Background
                                </button>
                            </h2>
                            <div id="collapseTwo" class="accordion-collapse collapse scroll"
                                aria-labelledby="headingTwo" data-bs-parent="#accordionHelp">
                                <div class="accordion-body">
                                    <strong>What is my standard?</strong> <br />
                                    You are probably wondering, “Who the heck gave you the authority to decide who is a
                                    man and who is a woman?” Well, no one gave me the authority; I am simply proclaiming
                                    the truth.<br /><br />
                                    The only one who has such authority would be the creator of all things, which is
                                    none other than Jesus, the Son of God. “He is the image of the invisible God, the
                                    firstborn of all creation. For by him all things were created, in heaven and on
                                    earth, visible and invisible, whether thrones or dominions or rulers or
                                    authorities—all things were created through him and for him. And he is before all
                                    things, and in him all things hold together.” (Colossians 1:15-17)<br /><br />
                                    Jesus, the Son of God, “emptied himself, by taking the form of a servant, being born
                                    in the likeness of men. And being found in human form, he humbled himself by
                                    becoming obedient to the point of death, even death on a cross, [and has risen from
                                    the dead]. Therefore God has highly exalted him and bestowed on him the name that is
                                    above every name, so that at the name of Jesus every knee should bow, in heaven and
                                    on earth and under the earth, and every tongue confess that Jesus Christ is Lord, to
                                    the glory of God the Father.” (Philippians 2:7-11 )<br /><br />
                                    He has been given all authority in heaven and on earth (Matthew 28:18), He is the
                                    only one with the authority to define man, woman, and gender.<br /><br />
                                    You can attempt to do your own thing, but you are His creation. You can say “there
                                    is no God”, but you are wrong. My suggestion is to submit to the Son of God, who is
                                    the true King, and follow Him.
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingThree">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                                    data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                    Contact
                                </button>
                            </h2>
                            <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree"
                                data-bs-parent="#accordionHelp">
                                <div class="accordion-body">
                                    <ul class="nav" id="contact-nav">
                                        <li class="nav-item">
                                            <a type="button" href="https://twitter.com/TechCoffeeLogic">
                                                <i class="bi bi-twitter"></i>
                                            </a>
                                        </li>
                                        <!-- <li class="nav-item">
                                                <a type="button" href="https://github.com/TechnicalCoffeeLogic">
                                                    <i class="bi bi-github"></i>
                                                </a>
                                            </li> -->
                                    </ul>
                                    <ul class="nav">
                                        <li class="nav-item" style="margin-right: 5px;">
                                            <p>Powered by Technical Coffee Logic, LLC</p>
                                        </li>
                                        <li class="nav-item" id="contact-nav-coffee">
                                            <i class="bi bi-cup"></i>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="modal-footer">
                </div>
            </div>
        </div>
    </div>

</template>

<style scoped>

#contact-nav {
    font-size: 2rem;
    justify-content: left;
    margin-bottom: 1rem;
}

#contact-nav-coffee {
    font-size: 1rem;
    justify-content: left;
    margin-bottom: 1rem;
    margin-right: .1rem;
}

.nav-item {
    display: flex;
    margin-right: 1rem
}

ul {
    list-style: none;
}

</style>