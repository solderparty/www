---
title: "Contact"
menu:
    main:
        weight: 99
layout: docs
---

{{< blocks/lead >}}
<h2>Get in touch</h2>
{{< /blocks/lead >}}

{{< blocks/section type="section" color="white">}}
<form id="contact-form" method="post" action="https://formspree.io/f/xjvjkkpj" role="form">
    <div class="controls">
        <div class="row">
            <div class="col-md-8 mx-auto">
                <div class="form-group">
                    <input id="form_name" type="text" name="name" class="form-control" placeholder="Name" required="required">
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-8 mx-auto">
                <div class="form-group">
                    <input id="form_email" type="text" name="email" class="form-control" placeholder="Email" required="required">
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-8 mx-auto">
                <div class="form-group">
                    <textarea id="form_message" name="message" class="form-control" placeholder="Message" rows="4" required="required"></textarea>
                </div>
            </div>
            <div class="col-md-8 mx-auto">
                <input type="submit" class="btn btn-success btn-send" value="Submit">
            </div>
        </div>
    </div>
</form>

{{< /blocks/section >}}
